# android canvas drawText 居中

```java
Rect targetRect = new Rect();
Paint paintText = new Paint(Paint.ANTI_ALIAS_FLAG);
String string = "Test String.";

paintText.setTextSize(40);
paintText.setColor(0xffff5555);
paintText.setTextAlign(Paint.Align.CENTER);

targetRect.set(0,30,130,130);

Paint.FontMetricsInt fontMetrics = paintText.getFontMetricsInt();
int baseline = (targetRect.bottom + targetRect.top - fontMetrics.bottom - fontMetrics.top) / 2;

canvas.drawText(string, targetRect.centerX(), baseline, paintText);

```