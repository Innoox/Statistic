# Statistic
Statystyka WM-I-Z-STAT  Semestr letni 2018/19  Laboratorium, grupa nr 1
    struct mColor
    {
      //..constructors and methods
    public:
      mColor(int rVal, int gVal, int bVal, float aVal) : r(rVal / 255.0f), g(gVal / 255.0f), b(bVal / 255.0f), a(aVal) {};
      mColor(std::string hexCode, float aVal) : r(0.0f), g(0.0f), b(0.0f), a(aVal) { colorInit(hexCode); };
      void colorInit(std::string hexCode)
      {
        r = static_cast<float>(std::strtol(hexCode.substr(1, 2).c_str(), 0, 16)) / 255.0f;
        g = static_cast<float>(std::strtol(hexCode.substr(3, 2).c_str(), 0, 16)) / 255.0f;
        b = static_cast<float>(std::strtol(hexCode.substr(5, 2).c_str(), 0, 16)) / 255.0f;
        mRGBA[0] = r;
        mRGBA[1] = g;
        mRGBA[2] = b;
        mRGBA[3] = a;
      }
      //..================================================================================================
      //..members
    public:
      float r{ 0.0f };
      float g{ 0.0f };
      float b{ 0.0f };
      float a{ 0.0f };
      float mRGBA[4]{ 0 };
      //..================================================================================================
    };
