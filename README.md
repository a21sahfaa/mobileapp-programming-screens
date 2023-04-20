
# Rapport

**Skriv din rapport här!**
först forkades samt cloneades appen screens,
sedan så skapade jag en ny aktivitet som heter button activity och i button activity.
nästa steg var att lägga en knapp i main activity så att när man trycker på knappen så ska det stå hej hej på min button activity.

Button button = findViewById(R.id.button);
button.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View view) {
Log.d("tag", "hej hej");

detta kod skrev jag på min main activity och i den första raden så hittar den button från main activity xml
andra raden så läggs det till en onclicklistener och i det så säger den att när knappen clickas så ska det printas ut hej hej.

nästa steg var att lägga data i intent för att starta en ny aktivitet i samma app. 

public void onClick(View view) {

                Intent intent = new Intent(MainActivity.this, ButtonActivity.class);
                intent.putExtra("name", "Daniel"); // Optional
                intent.putExtra("number", 1); // Optional
                startActivity(intent);

            }
när man klickar på knappen så ska en ny intetnt skapas som innehåller både aktiviteterna,
andra och tredje raden innehåller data som ska printas ut i button activity.
och sist ska den startas.

        snygg = findViewById(R.id.sahib);
        Bundle extras = getIntent().getExtras();
        if (extras != null) {
            String name = extras.getString("name");
            int number = extras.getInt("number");
            // Do something with the name and number

            snygg.setText(name + number);

        }
detta kod är från button activity. först gav jag min textview xml på buttonactivity en id som är sahib.

den första raden säger vi att snygg är lika med id som jag gav min textview.
andra raden hämtar vi intent och extras från main activity.
tredje raden säger vi om extras är inte lika med null så ska namnet från main activity skrivas ut samt number från main activity.
och sist så säger vi att textviewn ska skriva ut name + number.








![](android.png)
