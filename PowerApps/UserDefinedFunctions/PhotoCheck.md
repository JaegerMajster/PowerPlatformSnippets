udfVerifyProfilePhoto(ParamEmail: Text):Boolean =
    !IsBlank(ParamEmail) &&
    If(
        !IsError(
            Office365Users.UserPhotoMetadata(ParamEmail).HasPhoto
        ),
        Office365Users.UserPhotoMetadata(ParamEmail).HasPhoto
    )
;