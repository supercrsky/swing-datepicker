Swing下的日期选择控件，基于jdatepicker扩展，添加了时分秒功能。<br />
1.功能
  1)可设置年、月、日，显示星期几。
  2)可设置是否显示年、时分秒按钮。
  3)可自定义约束，如限制选择指定日期，指定星期几。
2.使用方法 <br />
JDatePicker picker = new JDatePicker(); <br />
picker.setTextEditable(true);<br />
picker.setShowYearButtons(true);<br />
//显示时分秒功能<br />
picker = new JDatePicker(new UtilDateModel());<br />
//日期范围限制,beginDate为日期类型的开始时间<br />
  RangeConstraint constraint = new RangeConstraint(beginDate,new Date());<br />
	picker.addDateSelectionConstraint(constraint);<br />
//取值<br />
 UtilDateModel dateModel =  (UtilDateModel) picker.getModel();<br />
 Date date = dateModel.getValue();<br />

