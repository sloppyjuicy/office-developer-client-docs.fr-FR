---
title: Obtention du chemin d’accès d’une version spécifique de MAPI pour le client de messagerie par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ee7fb05-cfb3-6b68-5a9a-1d6375f2e879
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1992e34a684a6b5894963eae0c299b21c064578c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346458"
---
# <a name="get-the-path-of-a-specific-version-of-mapi-for-the-default-mail-client"></a>Obtention du chemin d’accès d’une version spécifique de MAPI pour le client de messagerie par défaut

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique inclut un exemple de code C++ qui montre comment obtenir le chemin d'accès d'une version spécifique de MAPI utilisée par le client de messagerie par défaut sur un ordinateur. Les clients de messagerie MAPI ont une option pour spécifier dans le registre une DLL personnalisée que la bibliothèque de stub MAPI doit charger et distribuer les appels MAPI à. La clé de Registre à définir pour cette DLL personnalisée pour un client de messagerie par défaut est **MSIComponentID**, sous la clé **HKLM\Software\Clients\Mail** du client de messagerie par défaut. La fonction [FGetComponentPath](fgetcomponentpath.md) , exportée par la bibliothèque de stub MAPI, mapistub. dll, peut renvoyer le chemin d'accès à la version personnalisée de MAPI spécifiée par la clé de Registre **MSIComponentID** . 
  
Cet exemple de code inclut deux fonctions `HrGetRegMultiSZValueA` : `GetMAPISVCPath`et. La `GetMAPISVCPath` fonction utilise [FGetComponentPath](fgetcomponentpath.md) pour obtenir le chemin d'accès à la version personnalisée de MAPI. Il suppose que le client de messagerie par défaut est Microsoft Office Outlook 2007 et transmet à **FGetComponentPath** la valeur, `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, qu'Outlook 2007 définit comme ID de composant MAPI pour la clé de Registre **MSIComponentID** . 
  
> [!NOTE]
> En pratique, vous ne devez pas supposer la valeur `{FF1D0740-D227-11D1-A4B0-006008AF820E}`,, est toujours l'ID de composant de MAPI et la transmettre directement à **FGetComponentPath**. Pour savoir en toute fiabilité quelle version de MAPI Outlook utilise sur un ordinateur, vous devez lire à partir du registre la valeur de **MSIComponentID** et la transmettre à **FGetComponentPath**. 
  
La procédure ci-dessous `GetMAPISVCPath` décrit cette opération. 
  
1. Charge la bibliothèque de stubs MAPI, mapistub. dll, à partir du répertoire système.
    
2. Suppose que mapistub. dll exporte la fonction **FGetComponentPath** , il essaie d'obtenir l'adresse de cette fonction à partir de mapistub. dll. 
    
3. Si l'obtention de l'adresse à partir de mapistub. dll échoue, elle tente d'obtenir l'adresse à partir de Mapi32. dll.
    
4. Si l'obtention de l'adresse de **FGetComponentPath** réussit, elle ouvre le registre et `HrGetRegMultiSZValueA` utilise la fonction pour lire les valeurs de Registre sous **HKLM\Software\Clients\Mail\Microsoft Outlook**. 
    
5. Appelle **FGetComponentPath**, en spécifiant la `{FF1D0740-D227-11D1-A4B0-006008AF820E}`valeur, pour obtenir le chemin d'accès à la version de MAPI utilisée par Outlook 2007.
    
Notez que pour prendre en charge les copies localisées de MAPI pour l'anglais et les paramètres régionaux non anglais, l'exemple de code lit les valeurs des sous-clés **MSIApplicationLCID** et **MSIOfficeLCID** et appelle **FGetComponentPath**, en commençant par spécifier ** MSIApplicationLCID** en tant que *szQualifier* , puis en spécifiant de nouveau **MSIOfficeLCID** comme *szQualifier* . Pour plus d'informations sur les clés de Registre pour les clients de messagerie qui prennent en charge les langues autres que l'anglais, consultez [la rubrique Setting up the MSI Keys for your MAPI dll](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).
  
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


