---
title: Lien vers des fonctions MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400144"
---
# <a name="link-to-mapi-functions"></a>Lien vers des fonctions MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe trois méthodes de liaison : la liaison implicite, liaison explicite et un nouveau modèle hybride à l’aide de la bibliothèque Stub MAPI.
  
## <a name="implicit-linking"></a>Liaison implicite

Historiquement, l’appel de fonctions MAPI dans une application de messagerie toujours impliquée liaison à la bibliothèque Mapi32.lib. Cette partie de routage des appels MAPI à la bibliothèque stub MAPI Windows, Mapi32.dll qui puis transférer les appels à l’implémentation du client MAPI par défaut en cours d’exécution. Ce processus d’appel est appelé liaison implicite. Le côté gauche de la figure suivante montre un exemple de liaison implicite utilisée dans un processus d’appel de fonction MAPI. Le processus est initié par une application MAPI et implique la bibliothèque MAPI (Mapi32.lib) et le stub MAPI Windows (Mapi32.dll) et se termine par l’implémentation de client MAPI Outlook du stub MAPI (Msmapi32.dll).
  
**Comparaison de liaison implicites et explicites.**

![Comparaison de liaison implicites et explicites] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparaison de liaison implicites et explicites")
  
## <a name="explicit-linking"></a>Liaison explicite

Étant donné que le client MAPI par défaut prend en charge l’installation de la demande à l’aide de Windows Installer (MSI), vous pouvez développer des applications de messagerie directement sur le stub MAPI Outlook au lieu d’utiliser la bibliothèque MAPI et un stub MAPI Windows. Le côté droit de la figure précédente montre un exemple d’un processus d’appel de fonction MAPI, commençant par une application MAPI, recherchez le chemin d’accès et le nom de la DLL pour le stub MAPI Outlook (étape 2 dans la section suivante) et l’émission d’appels de fonction dans la (stub MAPI Outlook étape 3 dans la section suivante). La procédure suivante montre comment appeler des fonctions MAPI à l’aide de la liaison explicite. 
  
> [!NOTE]
> Ces informations sur la liaison explicite peuvent être superflues à vos besoins avec l’introduction de la MAPIStubLibrary.lib présenté dans la section suivante. Comme le modèle implicite, la nouvelle bibliothèque gère tout et implémente la logique de liaison explicite qui charge d’Outlook MAPI directement. 
  
Pour plus d’informations sur la liaison explicite, voir liaison explicitement.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Pour appeler les éléments de l’API MAPI sans la bibliothèque MAPI et le stub MAPI Windows

1. Dans votre fichier de programme, créez une liste globale des pointeurs fonction pour chaque élément MAPI API que vous utilisez. 
    
   L’exemple suivant montre cette étape.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Créez une fonction qui initialise les fonctions MAPI à lier à la DLL MAPI du client MAPI par défaut (par exemple, Msmapi32.dll de Microsoft Outlook). Dans cette fonction, procédez comme suit : 
    
    1. Charger mapi32.dll à partir du répertoire système approprié. 
        
       |||
       |:-----|:-----|
       |x64 ou x86 en mode natif  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 mode WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Appelez la fonction [FGetComponentPath](fgetcomponentpath.md) pour obtenir le chemin d’accès et le nom de la DLL qui implémente le sous-système MAPI. Pour plus d’informations, voir [Choisir une Version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Charger la DLL en appelant la fonction LoadLibrary. 
        
    4. Initialiser le tableau de pointeur de fonction MAPI en appelant la fonction GetProcAddress. 
        
    L’exemple suivant montre les étapes précédentes :
        
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

3. Enfin, appelez la fonction que vous avez créé à l’étape 2 dans votre application de messagerie avant d’effectuer des appels à des éléments de l’API de MAPI. 
    
   > [!CAUTION]
   > Vous devez annuler l’initialisation du sous-système MAPI avant la fermeture de votre application. 
  
   L’exemple suivant illustre cette étape : 
    
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

L’arrivée de Microsoft Outlook 2010 et 64 bits MAPI, extension maintenant de Microsoft Outlook 2013, nécessite plus que l’API 32 bits traditionnel d’implémentation complète. Un nouveau projet, la bibliothèque Stub MAPI, publié sur le site Web CodePlex fournit une solution de remplacement dans le désordre pour Mapi32.lib qui prend en charge la création d’applications MAPI 32 bits et 64 bits. MAPIStubLibrary.lib élimine le besoin pour une liaison explicite à MAPI, et ayant généré il, vous pouvez supprimer Mapi32.lib de vos paramètres de l’éditeur de liens, remplaçant par MAPIStubLibrary.lib ; aucune modification supplémentaire à votre code ne doit être exécutée. Il supprime également la nécessité d’écrire du code **LoadLibrary**et **GetProcAddress** **FreeLibrary** pour gérer la plus récente exporte inclus dans ce fichier de bibliothèque mais pas dans Mapi32.lib, ce qui serait nécessaire si vous avez utilisé une liaison explicite. 
  
Voici quelques-unes des nouvelles fonctions liées à partir de cette bibliothèque qui ne sont pas disponibles dans Mapi32.lib :
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Une autre méthode de l’incorporation de la bibliothèque Stub MAPI consiste à copier les fichiers sources, MapiStubLibrary.cpp et StubUtils.cpp, directement dans votre projet et supprimer aucune liaison à Mapi32.lib ainsi que le code qui lie explicitement à MAPI.
  
Pour accéder aux fichiers de bibliothèque de Stub MAPI et pour plus d’informations sur la façon de créer et intégrer à votre projet, ainsi que des questions sur cette bibliothèque comme quand et pourquoi utiliser, voir la [Bibliothèque Stub de MAPI](https://mapistublibrary.codeplex.com/documentation) sur le site CodePlex. 
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble de la programmation MAPI](mapi-programming-overview.md)
- [Installation du sous-système MAPI](installing-the-mapi-subsystem.md)
- [Installer les fichiers d’en-tête MAPI](how-to-install-mapi-header-files.md)
- [Choisir une version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Méthode de liaison à utiliser](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Liaison d’un exécutable à une DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Configuration des clés MSI pour votre DLL MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

