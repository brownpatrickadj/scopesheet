---
layout: default
title: Scope Form
---
<body>
  <h1>Submit Scope Sheet</h1>
  <form action="index.html" method="get">
    <label>Claim Number: <input name="claim_number" required></label><br>
    <label>Insured Name: <input name="insured_name" required></label><br>
    <label>Property Address: <input name="property_address"></label><br>
    <label>Date of Inspection: <input type="date" name="date_of_inspection"></label><br>
    <label>Time of Inspection: <input name="time_of_inspection"></label><br>
    <label>Persons Present: <input name="persons_present"></label><br>
    <label>Damage Description: <input name="damage_description"></label><br>
    <label>Estimated Cost: <input type="number" name="estimated_cost"></label><br>
    <label>Photo URL: <input name="photo_url"></label><br><br>
    <button type="submit">Submit</button>
  </form>
</body>
<style>
    body {
      font-family: sans-serif;
      max-width: 1000px;
      margin: auto;
      padding: 20px;
      background: #f9f9f9;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 20px;
    }
    th, td {
      border: 1px solid #aaa;
      padding: 8px;
      vertical-align: top;
    }
    th {
      background: #ddd;
    }
    input[type="text"], input[type="number"], textarea, select {
      width: 95%;
      padding: 6px;
      box-sizing: border-box;
    }
    textarea {
      height: 100px;
    }
  </style>
</head>
<body>

  <h1>Exterior Scope Sheet Form</h1>

  <form>
    <p>
      <label>Claim #: <input type="text" name="claim_number" required></label>
      <label>Policy Holder: <input type="text" name="policy_holder"></label>
      <label>Contractor: <input type="text" name="contractor"></label>
    </p>

    <fieldset>
      <legend><strong>Damage to elevations</strong></legend>
      Front: <input type="checkbox" name="front" value="yes">
      Right: <input type="checkbox" name="right" value="yes">
      Rear: <input type="checkbox" name="rear" value="yes">
      Left: <input type="checkbox" name="left" value="yes">
    </fieldset>

    <table>
      <tr>
        <th>Elevation:</th>
        <td><select name="elevation"><option>Front</option><option>Right</option><option>Rear</option><option>Left</option></select></td>
        <th>Structure:</th>
        <td><select name="structure"><option>Dwelling</option><option>Garage</option><option>Shed</option></select></td>
      </tr>
      <tr>
        <th>Gutters / Guards (Size/LF)</th>
        <td><input type="text" name="gutters"></td>
        <th>Screens (Size/Type)</th>
        <td><input type="text" name="screens"></td>
      </tr>
      <tr>
        <th>Downspouts (Size/LF)</th>
        <td><input type="text" name="downspouts"></td>
        <th>Windows (Size/Type/Materials)</th>
        <td><input type="text" name="windows"></td>
      </tr>
      <tr>
        <th>Fascia (Size/Type)</th>
        <td><input type="text" name="fascia"></td>
        <th>Doors (include Finish)</th>
        <td><input type="text" name="doors"></td>
      </tr>
      <tr>
        <th>Soffit / Soffit Vents (Type /SF)</th>
        <td><input type="text" name="soffit"></td>
        <th>Lights</th>
        <td><input type="text" name="lights"></td>
      </tr>
      <tr>
        <th>Gable / Dryer Vent(s)</th>
        <td><input type="text" name="gable"></td>
        <th>Awnings (Size/Type)</th>
        <td><input type="text" name="awnings"></td>
      </tr>
      <tr>
        <th>Siding / Masonry (Type /Finish)</th>
        <td><input type="text" name="siding"></td>
        <th>HVAC</th>
        <td><input type="text" name="hvac"></td>
      </tr>
      <tr>
        <th>Shutters (Size/Type)</th>
        <td><input type="text" name="shutters"></td>
        <th>Patio Cover / Carport</th>
        <td><input type="text" name="patio_cover"></td>
      </tr>
      <tr>
        <th>Window Wraps (Size/Type)</th>
        <td><input type="text" name="window_wraps"></td>
        <th>Fencing (LF) (Type/Finish)</th>
        <td><input type="text" name="fencing"></td>
      </tr>
      <tr>
        <th>Window Beading (LF)</th>
        <td><input type="text" name="window_beading"></td>
        <th>Other:</th>
        <td><input type="text" name="other_1"></td>
      </tr>
      <tr>
        <th>Other:</th>
        <td colspan="3"><input type="text" name="other_2"></td>
      </tr>
    </table>

    <label for="diagram">Diagram / Notes:</label><br>
    <textarea id="diagram" name="diagram_notes" placeholder="Enter any additional notes here..."></textarea>

    <br><br>
    <button type="submit">Submit</button>
  </form>

</body>
