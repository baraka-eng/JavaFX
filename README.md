//
// Source code recreated from a .class file by IntelliJ IDEA
// (powered by FernFlower decompiler)
//

package sample;

import javafx.application.Application;
import javafx.collections.FXCollections;
import javafx.collections.ObservableList;
import javafx.geometry.Insets;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.CheckBox;
import javafx.scene.control.ChoiceBox;
import javafx.scene.control.DatePicker;
import javafx.scene.control.ListView;
import javafx.scene.control.RadioButton;
import javafx.scene.control.TextField;
import javafx.scene.control.ToggleButton;
import javafx.scene.control.ToggleGroup;
import javafx.scene.layout.GridPane;
import javafx.scene.text.Text;
import javafx.stage.Stage;

public class Registration extends Application {
    public Registration() {
    }

    public void start(Stage stage) {
        Text nameLabel = new Text("Name");
        TextField nameText = new TextField();
        Text dobLabel = new Text("Date of birth");
        DatePicker datePicker = new DatePicker();
        Text genderLabel = new Text("Gender");
        ToggleGroup groupGender = new ToggleGroup();
        RadioButton maleRadio = new RadioButton("Male");
        maleRadio.setToggleGroup(groupGender);
        RadioButton femaleRadio = new RadioButton("Female");
        femaleRadio.setToggleGroup(groupGender);
        Text reservationLabel = new Text("Reservation");
        ToggleButton yes = new ToggleButton("yes");
        ToggleButton no = new ToggleButton("No");
        ToggleGroup groupReservation = new ToggleGroup();
        yes.setToggleGroup(groupReservation);
        no.setToggleGroup(groupReservation);
        Text technologieslabel = new Text("Technologies known");
        CheckBox javaCheckbox = new CheckBox("Java");
        javaCheckbox.setIndeterminate(false);
        CheckBox dotnetCheckBox = new CheckBox("DotNet");
        dotnetCheckBox.setIndeterminate(false);
        Text educationLabel = new Text("Educational Qualifications");
        ObservableList<String> names = FXCollections.observableArrayList(new String[]{"Engineering", "MCA", "MBA", "Graduation", "MTECH", "Mphil", "PhD"});
        ListView<String> educationListView = new ListView(names);
        Text locationLabel = new Text("Location");
        ChoiceBox locationChoiceBox = new ChoiceBox();
        locationChoiceBox.getItems().addAll(new Object[]{"Eldoret", "Nakuru", "Bungoma", "Kitale", "Nairobi", "Nairobi"});
        Button buttonRegister = new Button("register");
        GridPane gridPane = new GridPane();
        gridPane.setMinSize(500.0D, 500.0D);
        gridPane.setPadding(new Insets(10.0D, 10.0D, 10.0D, 10.0D));
        gridPane.setVgap(5.0D);
        gridPane.setHgap(5.0D);
        gridPane.add(nameLabel, 0, 0);
        gridPane.add(nameText, 1, 0);
        gridPane.add(dobLabel, 0, 1);
        gridPane.add(datePicker, 1, 1);
        gridPane.add(genderLabel, 0, 2);
        gridPane.add(maleRadio, 1, 2);
        gridPane.add(femaleRadio, 2, 2);
        gridPane.add(reservationLabel, 0, 3);
        gridPane.add(yes, 1, 3);
        gridPane.add(no, 2, 3);
        gridPane.add(technologieslabel, 0, 4);
        gridPane.add(javaCheckbox, 1, 4);
        gridPane.add(dotnetCheckBox, 2, 4);
        gridPane.add(educationLabel, 0, 5);
        gridPane.add(educationListView, 1, 5);
        gridPane.add(locationLabel, 0, 6);
        gridPane.add(locationChoiceBox, 1, 6);
        gridPane.add(buttonRegister, 2, 8);
        nameLabel.setStyle("-fx-font:normal bold 15px 'serif' ");
        dobLabel.setStyle("-fx-font:normal bold 15px 'serif' ");
        genderLabel.setStyle("-fx-font:normal bold 15px 'serif' ");
        reservationLabel.setStyle("-fx-font:normal bold 15px 'serif' ");
        technologieslabel.setStyle("-fx-font:normal bold 15px 'serif' ");
        educationLabel.setStyle("-fx-font:normal bold 15px 'serif' ");
        locationLabel.setStyle("-fx-font:normal bold 15px 'serif' ");
        gridPane.setStyle("-fx-background-color:BEIGE;");
        Scene scene = new Scene(gridPane);
        stage.setTitle("Registration Form");
        stage.setScene(scene);
        stage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
