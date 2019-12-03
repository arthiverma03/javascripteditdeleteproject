
  
  <label for="count">Book Count</label>
    <select (change)="onSelectcity($event)">
    <option>select</option>
      <option value="{{counts}}" *ngFor="let counts of apikey; let i = index;">{{counts}}</option>
    </select>
  
  <label for="count">Book Count</label>
    <select >
      <option value="{{counts}}" *ngFor="let counts of bookcount; let i = index;">{{counts}}</option>
    </select>
   





