<div class="container">
        <div [hidden]="submitted">
          <h1>Travelers Form</h1>
          <form (ngSubmit)="onSubmit($event)" #heroForm="ngForm">
                <div class="form-group">
                        <label for="power">Source</label>
                        <select class="form-control" id="power"
                                required
                                [(ngModel)]="model.power" name="power"
                                #power="ngModel">
                          <option *ngFor="let pow of powers" [value]="pow">{{pow}}</option>
                        </select>
                        <div [hidden]="power.valid || power.pristine" class="alert alert-danger">
                          Source is required
                        </div>
                      </div>
      
            <div class="form-group">
                    <label for="power">Destination</label>
                    <select class="form-control" id="power"
                            required
                            [(ngModel)]="model.power" name="power"
                            #power="ngModel">
                      <option *ngFor="let pow of powers" [value]="pow">{{pow}}</option>
                    </select>
                    <div [hidden]="power.valid || power.pristine" class="alert alert-danger">
                      Destination is required
                    </div>
                  </div>
                  <div class="form-group">
                      <label for="source_subject">Source Subject Name</label>
                      <select class="form-control" name="source_subject" id="source_subject" [(ngModel)]="model.source_subject" placeholder="Select source...">
                          <option *ngFor="let subject of subjects" [attr.value]="subject">{{subject}}</option>
                      </select>
                      
                  </div>
            <div class="form-group">
              <label for="power">Application</label>
              <select class="form-control" id="power"
                      required
                      [(ngModel)]="model.power" name="power"
                      #power="ngModel">
                <option *ngFor="let pow of powers" [value]="pow">{{pow}}</option>
                <option href="" routerLink="/create-new" role="button">
                    <a  href="" routerLink="/create-new" role="button">ADD NEW</a>
                </option>
              </select>
              <div [hidden]="power.valid || power.pristine" class="alert alert-danger">
                Application is required
              </div>
            </div>
            <div class="form-group">
            <button type="submit" class="btn btn-success" [disabled]="!heroForm.form.valid">Submit</button>
            </div>
            <div class="form-group">
            <a type="submit" class="btn btn-success" href="" routerLink="/create-new" role="button">ADD NEW</a>
            </div>
          </form>
        </div>
 
        <div [hidden]="!submitted">
          <h2>You submitted the following:</h2>
          <div class="row">
            <div class="col-xs-3">source</div>
            <div class="col-xs-9">{{ model.source }}</div>
          </div>
          <div class="row">
            <div class="col-xs-3">destination</div>
            <div class="col-xs-9">{{ model.destination }}</div>
          </div>
          <div class="row">
            <div class="col-xs-3">application</div>
            <div class="col-xs-9">{{ model.power }}</div>
          </div>
          <br>
        </div>
      </div>
      <style>
        .no-style .ng-valid {
        border-left: 1px  solid #CCC
      }
      
        .no-style .ng-invalid {
        border-left: 1px  solid #CCC
      }
      </style>
    
      
      
     
