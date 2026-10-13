# umangdoshi.github.io

// INTERENET PERMISSION
<uses-permission android:name="android.permission.INTERNET"/>

// API INTEGRATION
 final response = await http.post(Uri.parse(CA.Url_first+url),
        headers: {'Content-Type': 'application/json', 'Accept': 'application/json',
          'Authorization': 'Bearer ${CA.Token_Save}'}, body: parameter);

 var map = await json.decode(response.body);
  if (map['success'] == true) {}

//SIZECONFIG
  class SizeConfig {
  static MediaQueryData? _mediaQueryData;
  static double? screenWidth;
  static double? screenHeight;
  static double? blockSizeHorizontal;
  static double? blockSizeVertical;
  static double? _safeAreaHorizontal;
  static double? _safeAreaVertical;
  static double? safeBlockHorizontal;
  static double? safeBlockVertical;
  static double minwidth=500.00;
  static double? chartheight;
  static double? chartweight;

  void init(BuildContext context) {
    _mediaQueryData = MediaQuery.of(context);
    screenWidth = _mediaQueryData!.size.width;
    screenHeight = _mediaQueryData!.size.height;
    chartheight=_mediaQueryData!.size.height*0.35;
    chartweight=_mediaQueryData!.size.height*0.9;
    blockSizeHorizontal = screenWidth! / 100;
    blockSizeVertical = screenHeight! / 100;
    _safeAreaHorizontal = _mediaQueryData!.padding.left +
        _mediaQueryData!.padding.right;
    _safeAreaVertical = _mediaQueryData!.padding.top +
        _mediaQueryData!.padding.bottom;
    safeBlockHorizontal = (screenWidth! - _safeAreaHorizontal!) / 100;
    safeBlockVertical = (screenHeight! - _safeAreaVertical!) / 100;
  }
}

  
