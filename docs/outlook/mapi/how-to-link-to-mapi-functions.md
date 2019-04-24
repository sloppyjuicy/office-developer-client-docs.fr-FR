---
title: Lien vers les fonctions MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346881"
---
# <a name="link-to-mapi-functions"></a>Lien vers les fonctions MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe trois méthodes de liaison: liaison implicite, liaison explicite et nouveau modèle hybride à l'aide de la bibliothèque de stub MAPI.
  
## <a name="implicit-linking"></a>Liaison implicite

Traditionnellement, l'appel de fonctions MAPI dans une application de messagerie impliquait toujours la liaison à la bibliothèque Mapi32. lib. Cela comprenait les appels MAPI de routage vers la bibliothèque Windows MAPI stub, Mapi32. dll, qui a ensuite transféré les appels vers l'implémentation cliente MAPI par défaut au moment de l'exécution. Ce processus d'appel est appelé liaison implicite. Le côté gauche de la figure suivante montre un exemple de liaison implicite utilisée dans un processus d'appel de fonction MAPI. Le processus est initié par une application MAPI et implique la bibliothèque MAPI (Mapi32. lib) et le stub MAPI Windows (Mapi32. dll) et est terminé par l'implémentation du client MAPI Outlook du stub MAPI (msmapi32. dll).
  
**Comparaison de la liaison implicite et explicite.**

![Comparaison de la liaison implicite et explicite] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparaison de la liaison implicite et explicite")
  
## <a name="explicit-linking"></a>Liaison explicite

Étant donné que le client MAPI par défaut prend en charge l'installation à la demande à l'aide de Windows Installer (MSI), vous pouvez développer des applications de messagerie directement sur le stub MAPI Outlook au lieu d'utiliser la bibliothèque MAPI et le stub MAPI Windows. La partie droite de la figure ci-dessus illustre un exemple de processus d'appel de fonction MAPI, commençant par une application MAPI recherchant le chemin d'accès et le nom de la DLL du stub MAPI Outlook (étape 2 de la section suivante) et effectuant des appels de fonction dans le stub MAPI Outlook ( étape 3 de la section suivante). La procédure suivante montre comment appeler des fonctions MAPI à l'aide de la liaison explicite. 
  
> [!NOTE]
> Ces informations sur la liaison explicite peuvent être superflues en ce qui concerne l'introduction de MAPIStubLibrary. lib abordée dans la section suivante. Comme le modèle implicite, la nouvelle bibliothèque gère tout et implémente la logique de liaison explicite qui charge directement l'interface MAPI d'Outlook. 
  
Pour plus d'informations sur la liaison explicite, consultez la rubrique liaison explicite.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Pour appeler des éléments de l'API MAPI sans la bibliothèque MAPI et le stub MAPI Windows

1. Dans votre fichier de programme, créez une liste globale de pointeurs de fonction pour chaque élément d'API MAPI que vous utilisez. 
    
   L'exemple suivant illustre cette étape.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Créez une fonction qui initialise les fonctions MAPI pour établir un lien vers la DLL MAPI du client MAPI par défaut (par exemple, msmapi32. dll de Microsoft Outlook). Dans cette fonction, procédez comme suit: 
    
    1. Chargez le fichier Mapi32. dll à partir du répertoire système approprié. 
        
       |||
       |:-----|:-----|
       |x64 ou x86 en mode natif  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 sur le mode WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Appelez la fonction [FGetComponentPath](fgetcomponentpath.md) pour obtenir le chemin d'accès et le nom de la dll qui implémentent le sous-système MAPI. Pour plus d'informations, consultez [la rubrique choisir une version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Chargez la DLL en appelant la fonction LoadLibrary. 
        
    4. Initialiser le tableau de pointeur de fonction MAPI en appelant la fonction GetProcAddress. 
        
    L'exemple suivant montre les étapes précédentes:
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. Enfin, appelez la fonction que vous avez créée à l'étape 2 de votre application de messagerie avant d'effectuer des appels aux éléments de l'API MAPI. 
    
   > [!CAUTION]
   > Vous devez désinitialiser le sous-système MAPI avant de fermer votre application. 
  
   L'exemple suivant illustre cette étape: 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a>MAPIStubLibrary. lib

L'avènement de Microsoft Outlook 2010 et de l'interface MAPI 64 bits, qui s'étend désormais à Microsoft Outlook 2013, nécessite plus que l'API de 32 bits traditionnelle pour une implémentation complète. Un nouveau projet, la bibliothèque de stubs MAPI, publié sur le site Web CodePlex fournit un remplacement de la bibliothèque Mapi32. lib qui prend en charge la génération d'applications MAPI 32 bits et 64 bits. MAPIStubLibrary. lib élimine la nécessité de créer explicitement un lien vers MAPI et de l'avoir créé, vous pouvez supprimer Mapi32. lib de vos paramètres de l'éditeur de liens en le remplaçant par MAPIStubLibrary. lib; aucune autre modification de votre code n'est nécessaire. Elle élimine également la nécessité d'écrire du code **LoadLibrary**, **GetProcAddress**et **FreeLibrary** pour gérer les exportations ultérieures incluses dans ce fichier de bibliothèque, mais pas dans Mapi32. lib, ce qui serait nécessaire si vous utilisiez la liaison explicite. 
  
Certaines des nouvelles fonctions liées à cette bibliothèque et qui ne sont pas disponibles dans Mapi32. lib incluent les suivantes:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Une autre méthode d'incorporation de la bibliothèque de stub MAPI consiste à copier les fichiers source, MapiStubLibrary. cpp et StubUtils. cpp, directement dans votre projet et supprimer tout lien vers Mapi32. lib et tout code qui se lie explicitement à MAPI.
  
Pour accéder aux fichiers de bibliothèque stub MAPI et pour obtenir des informations sur la façon de les créer et de les intégrer dans votre projet, ainsi que des questions sur cette bibliothèque, comme quand et pourquoi l'utiliser, reportez-vous à la [bibliothèque de stub MAPI](https://mapistublibrary.codeplex.com/documentation) sur le site Codeplex. 
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la programmation MAPI](mapi-programming-overview.md)
- [Installation du sous-système MAPI](installing-the-mapi-subsystem.md)
- [Installer des fichiers d'en-tête MAPI](how-to-install-mapi-header-files.md)
- [Choisir une version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Détermination de la méthode de liaison à utiliser](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Liaison d'un exécutable à une DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Configuration des clés MSI pour votre DLL MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

