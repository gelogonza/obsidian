---
Course: C212 Java
---
```Java
interface IExpr {
		int eval();
	}
	
class Add implements IExpr {
private IExpr left;
private IExpr right;
Add(IExpr left, IExpr right) {
	this.left = left;
	this.right = right;
}

@Override
public int eval() {

}
```