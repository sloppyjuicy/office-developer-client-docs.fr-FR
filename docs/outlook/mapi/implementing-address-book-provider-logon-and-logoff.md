---
title: Implémentation de l'ouverture et de la fermeture de session du fournisseur de carnet d'adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438735"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implémentation de l'ouverture et de la fermeture de session du fournisseur de carnet d'adresses

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnets d'adresses prennent en charge la connexion et la fermeture de session en implémentant les méthodes de l'interface [IABProvider: IUnknown](iabprovideriunknown.md) . L'interface * * IABProvider * * hérite directement de **IUnknown** et n'ajoute que deux autres méthodes: **Logon** et **Shutdown**. 
  
## <a name="logoff"></a>Déconnexion

MAPI appellera la méthode [IABProvider:: Logon](iabprovider-logon.md) de votre fournisseur au début de chaque session et à chaque fois que votre fournisseur est ajouté au profil actuel et que le client prend en charge la reconfiguration dynamique. Lorsque MAPI appelle la méthode **IABProvider:: Logon** , votre fournisseur de carnet d'adresses commence son processus d'ouverture de session. 
  
**Pour implémenter IABProvider:: log**
  
1. Initialisez tous les pointeurs de paramètre de sortie passés par MAPI. 
    
2. Appelez la méthode **IUnknown:: AddRef** de l'objet de prise en charge pour incrémenter son décompte de références. 
    
3. Appelez la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) de l'objet de prise en charge pour ouvrir la section du profil qui contient les informations de configuration relatives à votre fournisseur. TransMettez NULL pour le paramètre _lpUID_ et l'indicateur MAPI_MODIFY si vous avez l'intention d'effectuer des modifications. 
    
4. Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la section Profil pour extraire les propriétés dont votre fournisseur a besoin pour l'ouverture de session, comme le nom du fichier de données ou de la table de base de données. 
    
5. Vérifiez que les propriétés sont disponibles et valides. Si nécessaire et autorisé, affiche une boîte de dialogue invitant l'utilisateur à effectuer des corrections ou des ajouts à des informations non valides ou manquantes et à appeler la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) de la section Profil pour enregistrer les modifications. Voici quelques-unes des propriétés communes qui doivent être disponibles: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Ne définissez pas **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). Au moment de la connexion, ces propriétés sont en lecture seule. 
  
6. Si une ou plusieurs propriétés de configuration ne sont pas disponibles, échoue et renvoie la valeur MAPI_E_UNCONFIGURED.
    
7. Appelez [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) pour enregistrer un [MAPIUID](mapiuid.md). Votre fournisseur peut créer une **MAPIUID** en procédant comme suit: 
    
   - Appel de la méthode [IMAPISupport:: NewUID](imapisupport-newuid.md) . 
    
   - Appel de UUIDGEN. EXE pour définir un GUID que votre fournisseur utilise pour inclure dans l'un de ses fichiers d'en-tête.
    
8. Si vous le souhaitez, enregistrez un **MAPIUID** nouvellement créé dans le profil actuel en appelant la méthode * * IMAPIProp:: SetProps * * de la section profile. 
    
9. Libérez la section profil en appelant sa méthode **IUnknown:: Release** . 
    
10. Instanciez un nouvel objet Logon et définissez le contenu du paramètre _lppABLogon_ sur l'adresse de ce nouvel objet. 
    
Étant donné qu'il est possible pour MAPI d'appeler votre méthode * * Logon * * plusieurs fois au cours d'une session, il est judicieux de prendre en charge cette possibilité dans votre implémentation en créant plusieurs objets Logon et en gardant à l'esprit chaque objet créé. La prise en charge de plusieurs appels **d'ouverture** de session permet à un utilisateur d'une application cliente, par exemple, de se connecter à une session avec des identités différentes ou d'utiliser différentes destinations de remise. 
  
**Shutdown** est appelé à la fin de la session. MAPI appelle votre méthode [IABProvider:: Shutdown](iabprovider-shutdown.md) comme l'une des dernières tâches impliquées dans l'arrêt d'une session. MAPI a libéré tous les objets d'ouverture de session de votre fournisseur et, lorsque votre fournisseur reçoit cet appel, il peut supposer qu'il s'agit du dernier appel qu'il recevra. Dans votre implémentation de **IABProvider:: Shutdown**, effectuez tout nettoyage final nécessaire. Par exemple, votre fournisseur peut appeler **MAPIDeinitIdle** s'il a appelé **MAPIInitIdle** pour utiliser le moteur inactif pendant la session ou la méthode **IUnknown:: Release** de tous les objets qui n'ont pas encore été libérés. 
  
Si votre fournisseur n'a pas de nettoyage final, son implémentation peut être composée d'une seule ligne de code: 
  
```cpp
return S_OK;

```


