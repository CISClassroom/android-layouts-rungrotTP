# รายงานผลการทดลอง

<นายรุ่งโรจน์  พลเยี่ยม> <603410060-4>

## Relative Layout

แสดง Control `title` และ `Detail`

```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".RelativeActivity">

    <EditText
        android:id="@+id/editText6"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/editText5"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name" />

    <EditText
        android:id="@+id/editText5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/editText6"
        android:text="Button" />
</RelativeLayout>
```

แอดทริบิ้วที่แสดงความสัมพันธ์ระหว่าง control ทั้งสอง

```xml
android:layout_below="@id/editText5" คำสั่งควบคุม ให้อยู่ด้านล่าง
```

## Linear Layout

แสดง Control `to`, `subject`, `tag` และ `message`

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".LinearActivity">


    <EditText
        android:id="@+id/editText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name" />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="horizontal">

        <EditText
            android:id="@+id/editText2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name" />

        <EditText
            android:id="@+id/editText3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name" />

        <EditText
            android:id="@+id/editText4"
            android:layout_width="match_parent"
            android:layout_height="238dp"
            android:ems="10"
            android:gravity="start|top"
            android:inputType="textMultiLine" />

        <Button
            android:id="@+id/button5"
            android:layout_width="185dp"
            android:layout_height="148dp"
            android:layout_weight="1"
            android:text="Button" />

    </LinearLayout>

</LinearLayout>
```

อธิบายความแตกต่างระหว่าง vertical และ horizontal orientation

```
// คำตอบ vertical คือ รูปแบบการจัดเรียงวัตถุ แบบตามแนวตั้ง
 horizontal orientation  คือ รูปแบบการจัดเรียงวัตถุ แบบตามแนวนอน
```

## Constrant Layout

จงออกแบบและสร้างหน้า Constrant layout สำหรับแสดงข้อมูลนักศึกษา ประกอบไปด้วย รูปโปรไฟล์ รูปพื้นหลัง ชื่อ-นามสกุล รหัสนักศึกษา และเกรดเฉลี่ยรวม

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".ConstranActivity">


    <TextView
        android:id="@+id/textView5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="321dp"
        android:layout_marginEnd="32dp"
        android:layout_marginRight="32dp"
        android:layout_marginBottom="200dp"
        android:text="นายรุ่งโรจน์  พลเยี่ยม"
        android:textColor="#000000"
        android:textSize="24sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.581"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/imageView2"
        app:layout_constraintVertical_bias="0.449"
        tools:ignore="MissingConstraints" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        app:layout_constraintTop_toTopOf="parent"
        app:srcCompat="@drawable/o"
        tools:layout_editor_absoluteX="0dp" />

    <ImageView
        android:id="@+id/imageView2"
        android:layout_width="185dp"
        android:layout_height="291dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="@+id/imageView"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.718"
        app:srcCompat="@drawable/oo"
        tools:ignore="MissingConstraints" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="เกรดเฉลี่ยรวม : 3.55"
        android:textColor="#001055"
        android:textSize="24sp"
        android:textStyle="bold"
        android:typeface="normal"
        app:fontFamily="sans-serif-thin"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.448"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView5"
        app:layout_constraintVertical_bias="0.673" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="347dp"
        android:layout_height="31dp"
        android:text="รหัสนักศึกษา  :603410155-3"
        android:textColor="#000000"
        android:textSize="24sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.75"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView5"
        app:layout_constraintVertical_bias="0.15" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
