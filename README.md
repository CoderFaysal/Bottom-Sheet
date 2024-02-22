# Bottom Sheet

### Create an XML File and Design you need

## XML Layout

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:padding="15dp"
    android:gravity="center_horizontal"
    android:orientation="vertical"
    android:background="@drawable/bottom_bg"
    >


    <ImageView
        android:id="@+id/close"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:src="@android:drawable/ic_menu_close_clear_cancel"
        />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Rakib Mahmud"
        android:textSize="18sp"
        android:textStyle="bold"
        android:textColor="#145E03"
        android:layout_marginTop="10dp"
        />


</LinearLayout>
```


### Create Click event in open Bottom Sheet 

## Initial Button

```
Button bottom_sheet = findViewById(R.id.bottom_sheet);
        
bottom_sheet.setOnClickListener(view -> {
  BOTTOM_SHEET();
});
```


## Create Method

```
private void BOTTOM_SHEET() {
  BottomSheetDialog bottomSheetDialog = new BottomSheetDialog(this);
  View view = LayoutInflater.from(this).inflate(R.layout.bottom_layout, null);

  ImageView close = view.findViewById(R.id.close);
        
  close.setOnClickListener(view1 -> {
    bottomSheetDialog.cancel();
  });

  bottomSheetDialog.setContentView(view);
  bottomSheetDialog.show();
  bottomSheetDialog.setCancelable(true);
}
```



© All Right Reserved By Coder Faysal







