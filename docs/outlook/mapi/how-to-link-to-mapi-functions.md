---
title: Lien vers les fonctions MAPI
description: Décrit les trois méthodes de liaison ; liaison implicite, liaison explicite et nouveau modèle hybride à l’aide de la bibliothèque STUB MAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
ms.openlocfilehash: ce3844568980d60160fa576d9bfef83360cd813f
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812782"
---
# <a name="link-to-mapi-functions"></a>Lien vers les fonctions MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe trois méthodes de liaison : la liaison implicite, la liaison explicite et un nouveau modèle hybride à l’aide de la bibliothèque STUB MAPI.
  
## <a name="implicit-linking"></a>Liaison implicite

Historiquement, l’appel de fonctions MAPI dans une application de messagerie implique toujours la liaison à la bibliothèque Mapi32.lib. Cela incluait le routage des appels MAPI vers la bibliothèque Windows stub MAPI, Mapi32.dll, qui a ensuite transféré les appels à l’implémentation du client MAPI par défaut au moment de l’exécution. Ce processus d’appel est appelé liaison implicite. Le côté gauche de la figure suivante montre un exemple de liaison implicite utilisée dans un processus d’appel de fonction MAPI. Le processus est initié par une application MAPI et implique la bibliothèque MAPI (Mapi32.lib) et le stub MAPI Windows (Mapi32.dll) et est terminé par l’implémentation Outlook client MAPI du stub MAPI (Msmapi32.dll).
  
**Comparaison des liaisons implicites et explicites.**

![Comparaison entre une liaison implicite et une liaison explicite](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparaison entre une liaison implicite et une liaison explicite")
  
## <a name="explicit-linking"></a>Liaison explicite

Étant donné que le client MAPI par défaut prend en charge l’installation à la demande à l’aide du programme d’installation de Windows (MSI), vous pouvez développer des applications de messagerie directement sur le stub MAPI Outlook au lieu d’utiliser la bibliothèque MAPI et Windows stub MAPI. Le côté droit de la figure précédente montre un exemple de processus d’appel de fonction MAPI, en commençant par une application MAPI recherchant le chemin d’accès et le nom de la DLL pour le stub MAPI Outlook (étape 2 dans la section suivante) et en effectuant des appels de fonction dans le Outlook stub MAPI (étape 3 dans la section suivante). La procédure suivante montre comment appeler des fonctions MAPI à l’aide d’une liaison explicite. 
  
> [!NOTE]
> Ces informations sur la liaison explicite peuvent être superflues à vos besoins avec l’introduction de MAPIStubLibrary.lib décrite dans la section suivante. Comme le modèle implicite, la nouvelle bibliothèque gère tout et implémente la logique de liaison explicite qui charge directement le MAPI de Outlook. 
  
Pour plus d’informations sur la liaison explicite, consultez Liaison explicite.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Pour appeler des éléments d’API MAPI sans la bibliothèque MAPI et le stub Windows MAPI

1. Dans votre fichier programme, créez une liste globale de pointeurs de fonction pour chaque élément d’API MAPI que vous utilisez. 
    
   L’exemple suivant illustre cette étape.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Créez une fonction qui initialise les fonctions MAPI pour établir un lien vers la DLL MAPI du client MAPI par défaut (par exemple, Msmapi32.dll de Microsoft Outlook). Dans cette fonction, procédez comme suit : 
    
    1. Chargez mapi32.dll à partir du répertoire système approprié. 
        
       |Propriété |Valeur |
       |:-----|:-----|
       |x64 ou x86 en mode natif  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 en mode WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Appelez la fonction [FGetComponentPath](fgetcomponentpath.md) pour obtenir le chemin d’accès et le nom de la DLL qui implémente le sous-système MAPI. Pour plus d’informations, consultez [Choisir une version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Chargez la DLL en appelant la fonction LoadLibrary. 
        
    4. Initialisez le tableau de pointeurs de fonction MAPI en appelant la fonction GetProcAddress. 
        
    L’exemple suivant montre les étapes précédentes :
        
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

3. Enfin, appelez la fonction que vous avez créée à l’étape 2 dans votre application de messagerie avant d’appeler des éléments de l’API MAPI. 
    
   > [!CAUTION]
   > Vous devez ne pas initialiser le sous-système MAPI avant de fermer votre application. 
  
   L’exemple suivant montre cette étape : 
    
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

## <a name="mapistublibrarylib"></a>MAPIStubLibrary.lib

L’avènement de Microsoft Outlook 2010 et de MAPI 64 bits, qui s’étend maintenant à la Microsoft Outlook 2013, nécessite plus que l’API 32 bits traditionnelle pour une implémentation complète. Un nouveau projet, la bibliothèque STUB MAPI, publié sur le site web CodePlex fournit un remplacement de liste déroulante pour Mapi32.lib qui prend en charge la création d’applications MAPI 32 bits et 64 bits. MAPIStubLibrary.lib élimine la nécessité de lier explicitement à MAPI et, après l’avoir créé, vous pouvez supprimer Mapi32.lib de vos paramètres d’éditeur de liens, en le remplaçant par MAPIStubLibrary.lib; aucune autre modification de votre code ne doit être nécessaire. Il élimine également la nécessité d’écrire du code **LoadLibrary**, **GetProcAddress** et **FreeLibrary** pour gérer les exportations plus récentes incluses dans ce fichier de bibliothèque, mais pas dans Mapi32.lib, ce qui serait nécessaire si vous utilisiez une liaison explicite. 
  
Voici quelques-unes des nouvelles fonctions liées à cette bibliothèque qui ne sont pas disponibles dans Mapi32.lib :
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Une autre méthode d’incorporation de la bibliothèque STUB MAPI consiste à copier les fichiers sources, MapiStubLibrary.cpp et StubUtils.cpp, directement dans votre projet et à supprimer toute liaison vers Mapi32.lib et tout code lié explicitement à MAPI.
  
Pour accéder aux fichiers de la bibliothèque STUB MAPI et pour plus d’informations sur la façon de la générer et de l’intégrer à votre projet, ainsi que des questions sur cette bibliothèque, telles que quand et pourquoi l’utiliser, consultez la [bibliothèque stub MAPI](https://mapistublibrary.codeplex.com/documentation) sur le site CodePlex. 
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la programmation MAPI](mapi-programming-overview.md)
- [Installation du sous-système MAPI](installing-the-mapi-subsystem.md)
- [Installer les fichiers d’en-tête MAPI](how-to-install-mapi-header-files.md)
- [Choisir une version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Détermination de la méthode de liaison à utiliser](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Liaison d’un exécutable à une DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Configuration des clés MSI pour votre DLL MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

