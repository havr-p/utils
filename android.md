Display some fragment at the startup of application: update viewModel of MainActivity to push your fragment
```
class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        if (savedInstanceState == null) {
            supportFragmentManager.beginTransaction()
                .replace(R.id.fragment_container, ScoreOverviewFragment())
                .commit()
        }
    }
}
```  
want to change drawable color dynamically? use android:backgroundTint
