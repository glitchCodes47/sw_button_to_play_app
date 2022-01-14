# sw_button_to_play_app

Intent intent = getPackageManager().getLaunchIntentForPackage("enter your package name");

if (intent != null) { // We found the activity now start the activity intent.addFlags(Intent.FLAG_ACTIVITY_NEW_TASK);

startActivity(intent);

} else {

// Bring user to the market or let them choose an app?

intent = new Intent(Intent.ACTION_VIEW); intent.addFlags(Intent.FLAG_ACTIVITY_NEW_TASK);

intent.setData(Uri.parse("market://details?id=" + "com.mobile.legends")); startActivity(intent);
}
