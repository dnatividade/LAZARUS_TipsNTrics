# LAZARUS_TipsNTrics

### Change color/font DBGrid row
```
procedure TForm1.DBGrid1DrawColumnCell(Sender: TObject; const Rect: TRect;
 DataCol: Integer; Column: TColumn; State: TGridDrawState);
begin
  if Table1.FieldByName('Salary').AsCurrency>36000 then
  begin
    DBGrid1.Canvas.Font.Color:= clRed;
    DBGrid1.Canvas.Font.Style:= [fsBold];
  end;    
  DBGrid1.DefaultDrawColumnCell(Rect, DataCol, Column, State);
end;

//SOURCE: https://www.thoughtco.com/change-coloring-in-tdbgrid-component-4077252
```

