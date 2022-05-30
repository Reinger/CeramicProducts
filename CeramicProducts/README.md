# CeramicProducts 

��������� ��� ��������� ����������� ����� ��� ������������ ������������ �������

## ����������

������ ��������� ������������ �������������� �����������, ������� ��� �� ���������� ���������� ���������� � ������� IISExpress

## ��������� �������

��� ���� ����� �������� ������� ��� ���������� �����������, ����������:
- � ������������� (Index.cshtml), �������� ����� ��� �������� ������ �� ������������
- � ����������� (HomeController.cs), �������� ������� � ��������� ����������

### �������������

���������� ��������, ���� ���������� ������� ��������� ��� �������. ��� ��������� ������� �� 3 ��������, ��� ������ ������������. ��� ����� ���� �������� ����������� �����:
```
    <p>
        <div class="row">
            <div class="col-md-4">
                ���� ������ ��� �����������:
                <input type="number" min="1" max="7" name="X1" style="width: 90px" placeholder="1-7" title="1-7" value="1" required />
            </div>
            <div class="col-md-4">
                �����������:
                <input type="number" min="18" max="30" step="0.01" name="X2" style="width: 90px" placeholder="�� 18-30" title="�� 18-30" value="18" required />
            </div>
            <div class="col-md-4">
                ��������� �� �������:
                <input type="number" min="25" max="90" step="0.01" name="X3" style="width: 90px" placeholder="% 25-90" title="% 25-90" value="25" required />
            </div>
        </div>
    </p>
```
� ������ ����� �������� ���������� � ���������:
- type="number" - ��������, ��� ��� �����
- min="1" - ����������� ��������
- max="7" - ������������ ��������
- step="0.01" - ��� ��� ���������� ��������
- name="X1" - �������� ��������� (����� ������ ��������, �� �������� ���������� �������� � ���������� �����������)
- style="width: 90px" - ������ ����
- placeholder="1-7" - ����������, ������� ������� � ������ ����
- title="1-7" - ����������, ������� ��������� ��� ��������� ������� �� ����
- value="1" - �������� �� ���������
- required - ���� ����������� ������ ���� ���������

```
<input type="number" min="25" max="90" step="0.01" name="X3" style="width: 90px" placeholder="% 25-90" title="% 25-90" value="25" required />
```

### ����������

���������� �������� ���������� ��������� � ���� �������: 
```
public ActionResult Index(int X1, string X2, string X3, string X4, string X5, string X6, string X7, string X8, string X9, string X10, string X11, string X12, string X13, string X14, string X15)
private double GetResult(double X1, double X2, double X3, double X4, double X5, double X6, double X7, double X8, double X9, double X10, double X11, double X12, double X13, double X14, double X15)
```

�������� �������������� ���������� �� ���������� ���� � ������������:
```
double value = GetResult(double.Parse(X1.ToString()), double.Parse(X2.Replace('.', ',')), double.Parse(X3.Replace('.', ',')), double.Parse(X4.Replace('.', ',')), double.Parse(X5.Replace('.', ',')),
                double.Parse(X6.Replace('.', ',')), double.Parse(X7.Replace('.', ',')), double.Parse(X8.Replace('.', ',')), double.Parse(X9.Replace('.', ',')), double.Parse(X10.Replace('.', ',')),
                 double.Parse(X11.Replace('.', ',')), double.Parse(X12.Replace('.', ',')), double.Parse(X13.Replace('.', ',')), double.Parse(X14.Replace('.', ',')), double.Parse(X15.Replace('.', ',')));
                 ```
�������� � ������ GetResult ������ ������� �� �����, ��� ���� �� ����� �������� ��������� � ����� �������.