---
layout: default
title: View Entry Form
---
<body>
  <h1>Edit Scope Sheet</h1>
  <div id="loading">Loading entry…</div>
  <form id="editForm" style="display:none; margin-top:20px;">
    <input type="hidden" id="id" />

    <label>Claim Number:
      <input type="text" id="claim_number" required>
    </label>

    <label>Insured Name:
      <input type="text" id="insured_name" required>
    </label>

    <label>Property Address:
      <input type="text" id="property_address">
    </label>

    <label>Date of Inspection:
      <input type="date" id="date_of_inspection">
    </label>

    <label>Time of Inspection:
      <input type="time" id="time_of_inspection">
    </label>

    <label>Persons Present:
      <input type="text" id="persons_present">
    </label>

    <label>Damage Description:
      <textarea id="damage_description" rows="4"></textarea>
    </label>

    <label>Estimated Cost:
      <input type="number" id="estimated_cost" step="0.01">
    </label>

    <label>Photo URL:
      <input type="url" id="photo_url">
    </label>

    <button type="submit">Save Changes</button>
    <button type="button" onclick="window.history.back()">Cancel</button>
  </form>

  <div id="message" style="margin-top:20px;"></div>

  <script>
    const supabase = window.supabase.createClient(
      'https://hobhuqbsiqboovhoipeo.supabase.co',
      'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImhvYmh1cWJzaXFib292aG9pcGVvIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NDgyODg3OTQsImV4cCI6MjA2Mzg2NDc5NH0.8iDzmTgUybI50e27fcIV0f3rjXxsxBOVKSH9btnY5dw'
    );

    window.onload = async () => {
      const params = new URLSearchParams(window.location.search);
      const id = params.get('id');
      if (!id) {
        document.getElementById('loading').textContent = '❌ No ID provided';
        return;
      }

      const { data, error } = await supabase
        .from('scope_sheets')
        .select('*')
        .eq('id', id)
        .single();

      if (error) {
        document.getElementById('loading').textContent = `❌ Error: ${error.message}`;
        return;
      }

      // Populate form
      document.getElementById('id').value              = data.id;
      document.getElementById('claim_number').value    = data.claim_number;
      document.getElementById('insured_name').value    = data.insured_name;
      document.getElementById('property_address').value= data.property_address;
      document.getElementById('date_of_inspection').value = data.date_of_inspection;
      document.getElementById('time_of_inspection').value = data.time_of_inspection;
      document.getElementById('persons_present').value    = data.persons_present;
      document.getElementById('damage_description').value = data.damage_description;
      document.getElementById('estimated_cost').value     = data.estimated_cost;
      document.getElementById('photo_url').value          = data.photo_url;

      document.getElementById('loading').style.display = 'none';
      document.getElementById('editForm').style.display = 'block';
    };

    document.getElementById('editForm').addEventListener('submit', async (e) => {
      e.preventDefault();
      const id = document.getElementById('id').value;

      const updates = {
        claim_number:       document.getElementById('claim_number').value,
        insured_name:       document.getElementById('insured_name').value,
        property_address:   document.getElementById('property_address').value,
        date_of_inspection: document.getElementById('date_of_inspection').value,
        time_of_inspection: document.getElementById('time_of_inspection').value,
        persons_present:    document.getElementById('persons_present').value,
        damage_description: document.getElementById('damage_description').value,
        estimated_cost:     parseFloat(document.getElementById('estimated_cost').value) || null,
        photo_url:          document.getElementById('photo_url').value
      };

      const { data, error } = await supabase
        .from('scope_sheets')
        .update(updates)
        .eq('id', id)
        .select()
        .single();

      const msg = document.getElementById('message');
      if (error) {
        msg.innerHTML = `<h2 style="color:red">❌ Update failed:</h2><pre>${error.message}</pre>`;
      } else {
        msg.innerHTML = `<h2 style="color:green">✅ Updated successfully!</h2>`;
        console.log(data);
      }
    });
  </script>
</body>
