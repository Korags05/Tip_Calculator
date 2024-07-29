# Tip Calculator 
activity_main.xml:

Root Element - LinearLayout:

xmlns:android, xmlns:app, and xmlns:tools: 
These attributes define XML namespaces for Android, app, and tools.

android:layout_width and android:layout_height: 
These attributes specify that the LinearLayout should match the parent's width and height.

android:background: 
Sets the background color of the layout.

android:orientation: 
Specifies the orientation of the LinearLayout (vertical in this case).

android:padding: 
Adds padding to the entire layout.

tools:context: 
Used for design-time tools; specifies the context of the layout.

ImageView:
Displays an image with a specified source (@drawable/tip_calculator__1_).

TextView (Bill):
Displays the text "Bill" and has black text color.

EditText (et_bill):
Allows the user to input a decimal number (for the bill amount).
Initial hint text is set to "100.00".

TextView (Tip%):
Displays the text "Tip%" with black text color.

LinearLayout (for Tip buttons and display):
Contains three elements: two buttons (b_tip_minus and b_tip_plus) for decreasing/increasing the tip percentage, and a TextView (tv_tip) displaying the current tip percentage.

TextView (People):
Displays the text "People" with black text color.

LinearLayout (for People buttons and display):
Similar to the LinearLayout for tip, it contains buttons (b_people_minus and b_people_plus) and a TextView (tv_people) for decreasing/increasing the number of people.

Button (Calculate):
Triggers the calculation of the tip and total amount.

TextView (Tip):
Displays the text "Tip" with black text color.

TextView (tv_tip_output):
Initially displays "Press Calculate" and later shows the calculated tip amount.

TextView (Total):
Displays the text "Total" with black text color.

TextView (tv_total_output):
Initially displays "Press Calculate" and later shows the calculated total amount.


MainActivity.java

Variable Declarations:
  Variables are declared for various UI elements (EditText, TextViews, and Buttons).
  Additional variables are declared to store values related to tip percentage, number of people, initial bill amount, and calculated tip and total amounts.

onCreate Method:
  The onCreate method is called when the activity is first created.
  It initializes the UI elements by finding them using their respective IDs from the XML layout.

Calculate Button Click Listener:
  When the "Calculate" button is clicked, the onClick method is executed.
  It retrieves the bill amount entered by the user and performs calculations for tip and total amounts.
  The results are then formatted and displayed in the respective TextViews.

Calculation Logic:
  The entered bill amount is converted to a double, formatted, and displayed back in the EditText.
  Tip calculation is performed based on the entered tip percentage.
  If the number of people is greater than 1, the tip and total amounts are divided by the number of people for a per-person display.

Tip and People Button Click Listeners:
  Separate click listeners are set for buttons that adjust tip percentage, increase/decrease the number of people, and update the corresponding TextViews.


In short,The code initializes UI elements, sets click listeners, and calculates tip and total amounts for a tip calculator, allowing users to input bill amounts, 
adjust tip percentages, and view results.
