---
title: Récupérer le corps du message dans un format RTF compressé et le convertir au format natif
description: Cet article explique comment récupérer le corps d’un message en RTF compressé et comment le convertir en son format natif.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9408da71-4abf-60cf-5412-58c5ceeb2205
ms.openlocfilehash: 76887599bdf36b33266da2c42bbe62c6f0f96e17
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816926"
---
# <a name="retrieve-body-of-message-in-compressed-rtf-and-convert-to-its-native-format"></a>Récupérer le corps du message dans un format RTF compressé et le convertir au format natif

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cet exemple de code dans Microsoft C++ vous montre comment utiliser la fonction Microsoft Outlook 2010 exportée ou Microsoft Outlook 2013 [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) pour accéder au corps d’un message encapsulé dans rtF compressé et obtenir le corps dans son format natif. 
  
```cpp
//These are definitions for the WrapCompressedRTFStreamEx function. 
typedef HRESULT (STDMETHODCALLTYPE WRAPCOMPRESSEDRTFSTREAMEX) ( 
    LPSTREAM lpCompressedRTFStream, CONST RTF_WCSINFO * pWCSInfo, LPSTREAM * lppUncompressedRTFStream, RTF_WCSRETINFO * pRetInfo); 
typedef WRAPCOMPRESSEDRTFSTREAMEX *LPWRAPCOMPRESSEDRTFSTREAMEX; 
 
HRESULT TestWrapCompressedRTFStreamEx(LPMESSAGE lpMsg) 
{ 
    HRESULT         hRes = S_OK; 
    LPSTREAM        lpCompressed = NULL; 
    LPSTREAM        lpUncompressed = NULL; 
    char            szBody[1024] = {0}; 
    ULONG           ulRead = 0; 
    RTF_WCSINFO     wcsinfo = {0}; 
    RTF_WCSRETINFO  retinfo = {0}; 
    LPSPropValue    lpPropCPID = NULL; 
 
    retinfo.size = sizeof(RTF_WCSRETINFO); 
 
    wcsinfo.size = sizeof(RTF_WCSINFO); 
    wcsinfo.ulFlags = MAPI_NATIVE_BODY; 
    wcsinfo.ulOutCodePage = 0; 
 
    // Retrieve the value of the Internet code page. 
    // Pass this value to the WrapCompressedRTFStreamEx function. 
    // If the property is not found, the default is 0. 
    if(SUCCEEDED(hRes = HrGetOneProp(lpMsg, PR_INTERNET_CPID, &lpPropCPID))) 
    { 
        wcsinfo.ulInCodePage = lpPropCPID->Value.l; 
    } 
 
    // Open the compressed RTF stream. 
    if(SUCCEEDED(hRes = lpMsg->OpenProperty(PR_RTF_COMPRESSED, 
                                         &IID_IStream, 
                                         STGM_READ | STGM_DIRECT, 
                                         0, 
                                         (LPUNKNOWN*)&lpCompressed))) 
    { 
 
        // Notice that the WrapCompressedRTFStreamEx function has been loaded 
        // by using the GetProcAddress function into pfnWrapEx. 
 
        // Call the WrapCompressedRTFStreamEx function. 
        if(SUCCEEDED(hRes = pfnWrapEx(lpCompressed, 
                                   &wcsinfo, 
                                   &lpUncompressed, 
                                   &retinfo))) 
        { 
 
            printf("Body's native type is: "); 
 
            // Check what the native body type is. 
            switch(retinfo.ulStreamFlags) 
            { 
            case MAPI_NATIVE_BODY_TYPE_RTF: 
                printf("MAPI_NATIVE_BODY_TYPE_RTF\n"); 
                break; 
            case MAPI_NATIVE_BODY_TYPE_HTML: 
                printf("MAPI_NATIVE_BODY_TYPE_HTML\n"); 
                break; 
            case MAPI_NATIVE_BODY_TYPE_PLAINTEXT: 
                printf("MAPI_NATIVE_BODY_TYPE_PLAINTEXT\n"); 
                break; 
            default: 
                printf("UNKNOWN\n"); 
            } 
 
            // Read the first 1,000 characters out of the stream. 
            if(SUCCEEDED(hRes = lpUncompressed->Read(szBody, 1024, &ulRead))) 
            { 
                printf("First %d characters of the native body stream:\n%s\n", ulRead, szBody); 
            } 
        } 
    } 
 
    MAPIFreeBuffer(lpPropCPID); 
    if(lpUncompressed)lpUncompressed->Release(); 
    if(lpCompressed)lpCompressed->Release(); 
 
    return hRes; 
} 

```


