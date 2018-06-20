---
title: Obtenir le chemin d’accès d’une version spécifique de MAPI pour le client de messagerie par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ee7fb05-cfb3-6b68-5a9a-1d6375f2e879
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 277505beb11dbc2b32b7e970c2bcf2a34dbdf00b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783463"
---
# <a name="get-the-path-of-a-specific-version-of-mapi-for-the-default-mail-client"></a>Obtenir le chemin d’accès d’une version spécifique de MAPI pour le client de messagerie par défaut

**S’applique à**: Outlook 
  
Cette rubrique inclut un exemple de code en langage C++ qui montre comment obtenir le chemin d’accès d’une version de MAPI est utilisé par le client de messagerie par défaut sur un ordinateur spécifique. Clients de messagerie MAPI ont une option pour spécifier dans le Registre des appels vers une DLL personnalisée que la bibliothèque stub MAPI doit charger et distribuer MAPI. La clé de Registre à définir pour cette DLL personnalisée pour un client de messagerie par défaut est **MSIComponentID**, sous la clé **HKLM\Software\Clients\Mail** du client de messagerie par défaut. La fonction [FGetComponentPath](fgetcomponentpath.md) , exportée par la bibliothèque stub MAPI, mapistub.dll, peut renvoyer le chemin d’accès à la version personnalisée de MAPI spécifié par la clé de Registre **MSIComponentID** . 
  
Cet exemple de code comprend deux fonctions : `HrGetRegMultiSZValueA` et `GetMAPISVCPath`. Le `GetMAPISVCPath` fonction utilise [FGetComponentPath](fgetcomponentpath.md) pour obtenir le chemin d’accès à la version personnalisée de MAPI. Il suppose que le client de messagerie par défaut est Microsoft Office Outlook 2007 et passe la valeur, **FGetComponentPath** `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, qui définit des Outlook 2007 comme le composant d’ID de MAPI pour la clé de Registre **MSIComponentID** . 
  
> [!NOTE]
> En pratique, vous ne devez pas considérer la valeur, `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, est toujours le composant ID de MAPI et passer directement à **FGetComponentPath**. Pour fiable savoir quelle version d’Outlook MAPI utilise sur un ordinateur, vous devez lire à partir du Registre la valeur de **MSIComponentID** et passez-le à **FGetComponentPath**. 
  
Les étapes suivantes décrivent comment `GetMAPISVCPath` effectue cette action. 
  
1. Charge la bibliothèque stub MAPI, mapistub.dll, à partir du répertoire du système.
    
2. Suppose que mapistub.dll exporte la fonction **FGetComponentPath** , il essaie d’obtenir l’adresse de cette fonction mapistub.dll. 
    
3. Si l’obtention de l’adresse de mapistub.dll échoue, il essaie d’obtenir l’adresse mapi32.dll.
    
4. Si l’obtention de l’adresse du **FGetComponentPath** réussit, il ouvre le Registre et utilise le `HrGetRegMultiSZValueA` fonction permettant de lire les valeurs de Registre sous **HKLM\Software\Clients\Mail\Microsoft Outlook**. 
    
5. Appelle **FGetComponentPath**, spécifiant la valeur, `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, afin d’obtenir le chemin d’accès à la version de MAPI qui utilise Outlook 2007.
    
Notez que pour prendre en charge les copies localisées de MAPI pour l’anglais et des paramètres régionaux autres que l’anglais, l’exemple de code lit les valeurs pour les sous-clés **MSIApplicationLCID** et **MSIOfficeLCID** et appelle **FGetComponentPath**, spécifiant tout d’abord ** MSIApplicationLCID** en tant que *szQualifier* , puis à nouveau si vous spécifiez **MSIOfficeLCID** comme *szQualifier* . Pour plus d’informations sur les clés de Registre pour les clients de messagerie qui prennent en charge des langues, voir [Paramètre Up the MSI clés pour votre DLL MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).
  
```cpp
// HrGetRegMultiSZValueA 
// Get a REG_MULTI_SZ registry value - allocating memory using new to hold it. 
void HrGetRegMultiSZValueA( 
    IN HKEY hKey, // the key. 
    IN LPCSTR lpszValue, // value name in key. 
    OUT LPVOID* lppData) // where to put the data. 
{ 
    *lppData = NULL; 
    DWORD dwKeyType = NULL;       
    DWORD cb = NULL; 
    LONG lRet = 0; 
    
    // Get its size 
    lRet = RegQueryValueExA( 
        hKey, 
        lpszValue, 
        NULL, 
        &amp;dwKeyType, 
        NULL, 
        &amp;cb); 
 
    if (ERROR_SUCCESS == lRet &amp;&amp; cb &amp;&amp; REG_MULTI_SZ == dwKeyType) 
    { 
        *lppData = new BYTE[cb]; 
       
        if (*lppData) 
        { 
            // Get the current value 
            lRet = RegQueryValueExA( 
                hKey,  
                lpszValue,  
                NULL,  
                &amp;dwKeyType,  
                (unsigned char*)*lppData,  
                &amp;cb); 
          
            if (ERROR_SUCCESS != lRet) 
            { 
                delete[] *lppData; 
                *lppData = NULL; 
            } 
        } 
    } 
} 
 
typedef BOOL (STDAPICALLTYPE FGETCOMPONENTPATH) ( 
    LPSTR szComponent, 
    LPSTR szQualifier, 
    LPSTR szDllPath, 
    DWORD cchBufferSize, 
    BOOL fInstall); 
typedef FGETCOMPONENTPATH FAR * LPFGETCOMPONENTPATH;  
 
/////////////////////////////////////////////////////////////////////////////// 
// Function name   : GetMAPISVCPath 
// Description       : This will get the correct path to the MAPISVC.INF file. 
// Return type      : void  
// Argument         : LPSTR szMAPIDir - Buffer to hold the path to the MAPISVC file. 
//                    ULONG cchMAPIDir - size of the buffer 
void GetMAPISVCPath(LPSTR szMAPIDir, ULONG cchMAPIDir) 
{ 
    HRESULT hRes = S_OK; 
    UINT uiRet = 0; 
    LONG lRet = 0; 
    BOOL bRet = true; 
    
    szMAPIDir[0] = &apos;\0&apos;; // Terminate string at position 0, safer if fail below 
    
    CHAR szSystemDir[MAX_PATH+1] = {0}; 
    
    // Get the system directory path 
    // (mapistub.dll and mapi32.dll reside here) 
    uiRet = GetSystemDirectoryA(szSystemDir, MAX_PATH); 
    if (uiRet &gt; 0) 
    { 
        CHAR szDLLPath[MAX_PATH+1] = {0}; 
       
        hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, &quot;%s\\%s&quot;,  
            szSystemDir, &quot;mapistub.dll&quot;); 
        if (SUCCEEDED(hRes)) 
        { 
            LPFGETCOMPONENTPATH pfnFGetComponentPath = NULL; 
          
            HMODULE hmodStub = 0; 
            HMODULE hmodMapi32 = 0; 
          
            // Load mapistub.dll 
            hmodStub = LoadLibraryA(szDLLPath); 
            if (hmodStub) 
            {    
                // Get the address of FGetComponentPath from the mapistub 
                pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                    hmodStub, &quot;FGetComponentPath&quot;); 
            } 
          
            // If failed to get the address of FGetComponentPath, 
            // try mapi32.dll 
            if (!pfnFGetComponentPath) 
            { 
                hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, &quot;%s\\%s&quot;, 
                    szSystemDir, &quot;mapi32.dll&quot;); 
                if (SUCCEEDED(hRes)) 
                { 
                    // Load mapi32.dll 
                    hmodMapi32 = LoadLibraryA(szDLLPath); 
                    if (hmodMapi32) 
                    { 
                        // Get the address of FGetComponentPath from mapi32 
                        pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                            hmodMapi32, &quot;FGetComponentPath&quot;); 
                    } 
                 } 
            } 
            if (pfnFGetComponentPath) 
            { 
                LPSTR szAppLCID = NULL; 
                LPSTR szOfficeLCID = NULL; 
                HKEY hMicrosoftOutlook = NULL; 
             
                lRet = RegOpenKeyEx( 
                    HKEY_LOCAL_MACHINE, 
                    _T(&quot;Software\\Clients\\Mail\\Microsoft Outlook&quot;), 
                    NULL, 
                    KEY_READ, 
                    &amp;hMicrosoftOutlook); 
             
                if (ERROR_SUCCESS == lRet &amp;&amp; hMicrosoftOutlook) 
                { 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, &quot;MSIApplicationLCID&quot;, (LPVOID*) &amp;szAppLCID); 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, &quot;MSIOfficeLCID&quot;, (LPVOID*) &amp;szOfficeLCID); 
                } 
             
                // Only passing a fixed value as the component ID for MAPI in this example 
                // In practice, must read from the registry the value of MSIComponentID 
                if (szAppLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                        &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, szAppLCID, szMAPIDir, cchMAPIDir, true); 
                } 
                if ((!bRet || szMAPIDir[0] == _T(&apos;\0&apos;)) &amp;&amp; szOfficeLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                    &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, szOfficeLCID, szMAPIDir, cchMAPIDir, true); 
                } 
                if (!bRet || szMAPIDir[0] == _T(&apos;\0&apos;)) 
                { 
                    bRet = pfnFGetComponentPath( 
                        &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, NULL, szMAPIDir, cchMAPIDir, true); 
                } 
             
                // Got the path to msmapi32.dll - need to strip it 
                if (bRet &amp;&amp; szMAPIDir[0] != _T(&apos;\0&apos;)) 
                { 
                    LPSTR lpszSlash = NULL; 
                    LPSTR lpszCur = szMAPIDir; 
                
                    for (lpszSlash = lpszCur; *lpszCur; lpszCur = lpszCur++) 
                    { 
                        if (*lpszCur == _T(&apos;\\&apos;)) lpszSlash = lpszCur; 
                    } 
                   *lpszSlash = _T(&apos;\0&apos;); 
                } 
 
                delete[] szOfficeLCID; 
                delete[] szAppLCID; 
                if (hMicrosoftOutlook) RegCloseKey(hMicrosoftOutlook);       
            } 
             
            // If FGetComponentPath returns FALSE or if 
            // it returned nothing, or if failed to find an 
            // address of FGetComponentPath, then 
            // just default to the system directory 
            if (!bRet || szMAPIDir[0] == &apos;\0&apos;) 
            { 
                hRes = StringCchPrintfA( 
                    szMAPIDir, cchMAPIDir,&quot;%s&quot;, szSystemDir); 
            } 
          
            if (szMAPIDir[0] != _T(&apos;\0&apos;)) 
            { 
                hRes = StringCchPrintfA( 
                    szMAPIDir, cchMAPIDir, &quot;%s\\%s&quot;, szMAPIDir, &quot;MAPISVC.INF&quot;); 
            } 
          
            if (hmodMapi32) FreeLibrary(hmodMapi32); 
            if (hmodStub) FreeLibrary(hmodStub); 
        } 
    }    
}

```


