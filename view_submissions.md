---
layout: default
title: View Submissions
---
<body>
  <h1>Submitted Scope Sheets</h1>
  <div id="loading">Loading...</div>
  <table id="submissions" style="display: none;">
    <thead>
      <tr>
        <th>ID</th>
        <th>Claim #</th>
        <th>Insured</th>
        <th>Address</th>
        <th>Date</th>
        <th>Time</th>
        <th>Cost</th>
      </tr>
    </thead>
    <tbody></tbody>
  </table>

  <script>
    const supabase = window.supabase.createClient(
      'https://hobhuqbsiqboovhoipeo.supabase.co',
      'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImhvYmh1cWJzaXFib292aG9pcGVvIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NDgyODg3OTQsImV4cCI6MjA2Mzg2NDc5NH0.8iDzmTgUybI50e27fcIV0f3rjXxsxBOVKSH9btnY5dw'
    );

    window.onload = async () => {
      const { data, error } = await supabase
        .from('scope_sheets')
        .select('id, claim_number, insured_name, property_address, date_of_inspection, time_of_inspection, estimated_cost')
        .order('id', { ascending: false });

      if (error) {
        document.getElementById('loading').textContent = `❌ Error: ${error.message}`;
        return;
      }

      const table = document.getElementById('submissions');
      const tbody = table.querySelector('tbody');
      document.getElementById('loading').style.display = 'none';
      table.style.display = 'table';

      data.forEach(entry => {
        const row = document.createElement('tr');
        row.style.cursor = 'pointer';
        row.addEventListener('click', () => {
          // redirect to individual view
          window.location.href = `view_entry.html?id=${entry.id}`;
        });
        row.innerHTML = `
          <td>${entry.id}</td>
          <td>${entry.claim_number}</td>
          <td>${entry.insured_name}</td>
          <td>${entry.property_address}</td>
          <td>${entry.date_of_inspection}</td>
          <td>${entry.time_of_inspection}</td>
          <td>${entry.estimated_cost}</td>
        `;
        tbody.appendChild(row);
      });
    };
  </script>
</body>
