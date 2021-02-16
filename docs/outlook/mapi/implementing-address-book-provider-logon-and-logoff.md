---
title: Mise en œuvre de l’logo et de la ffage du fournisseur de carnet d’adresses
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
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Mise en œuvre de l’logo et de la ffage du fournisseur de carnet d’adresses

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnets d’adresses peuvent prendre en charge l’ouverture de session et la vidage de session en implémentant les méthodes de l’interface [IABProvider : IUnknown.](iabprovideriunknown.md) L’interface ** IABProvider ** hérite directement **d’IUnknown** et n’ajoute que deux autres méthodes : **Logon** et **Shutdown**. 
  
## <a name="logoff"></a>Déconnexion

MAPI appelle la méthode [IABProvider::Logon](iabprovider-logon.md) de votre fournisseur au début de chaque session et chaque fois que votre fournisseur est ajouté au profil actuel et que le client prend en charge la reconfiguration dynamique. Lorsque MAPI appelle **la méthode IABProvider::Logon,** votre fournisseur de carnet d’adresses commence son processus d’accès. 
  
**Pour implémenter IABProvider::Log**
  
1. Initialiser tous les pointeurs de paramètre de sortie transmis par MAPI. 
    
2. Appelez la méthode **IUnknown::AddRef** de l’objet de support pour incrémenter son nombre de références. 
    
3. Appelez la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) de l’objet de support pour ouvrir la section du profil qui contient des informations de configuration sur votre fournisseur. Passez null pour le  _paramètre lpUID_ et l’MAPI_MODIFY si vous avez l’intention d’apporter des modifications. 
    
4. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la section de profil pour récupérer les propriétés dont votre fournisseur a besoin pour l’accès, telles que le nom du fichier de données ou de la table de base de données. 
    
5. Vérifiez que les propriétés sont toutes disponibles et valides. Si nécessaire et autorisé, affichez une boîte de dialogue pour demander à l’utilisateur d’apporter des corrections ou des ajouts à des informations non valides ou manquantes et appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la section de profil pour enregistrer les modifications. Voici quelques-unes des propriétés courantes qui doivent être disponibles : 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Ne définissez **pas PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). Au moment de l’logo, ces propriétés sont en lecture seule. 
  
6. Si une ou plusieurs propriétés de configuration ne sont pas disponibles, échouez et renvoyez la valeur MAPI_E_UNCONFIGURED.
    
7. Appelez [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire [un MAPIUID](mapiuid.md). Votre fournisseur peut créer un **MAPIUID** en : 
    
   - Appel de [la méthode IMAPISupport::NewUID.](imapisupport-newuid.md) 
    
   - Appel de lUUIDGEN.EXE pour définir un GUID que votre fournisseur utilise pour inclure dans l’un de ses fichiers d’en-tête.
    
8. Si vous le souhaitez, enregistrez un **MAPIUID** nouvellement créé dans le profil actuel en appelant la méthode ** IMAPIProp::SetProps ** de la section de profil. 
    
9. Publiez la section profil en appelant **sa méthode IUnknown::Release.** 
    
10. Ins instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object. 
    
Étant donné qu’il est possible pour MAPI d’appeler votre méthode ** Logon ** plusieurs fois au cours d’une session, il est judicieux de prendre en charge cette possibilité dans votre implémentation en étant en mesure de créer plusieurs objets d’ouverture de session et de suivre chaque objet créé. La prise **en** charge de plusieurs appels d’ouverture de session permet à un utilisateur d’une application cliente, par exemple, de se connecter à une session avec différentes identités ou d’utiliser des destinations de remise différentes. 
  
**L’arrêt** est appelé à la fin de la session. MAPI appelle votre [méthode IABProvider::Shutdown](iabprovider-shutdown.md) comme l’une des dernières tâches impliquées dans l’arrêt d’une session. MAPI a libéré tous les objets d’accès de votre fournisseur et, lorsque celui-ci reçoit cet appel, il peut supposer qu’il s’agit du dernier appel qu’il recevra. Dans votre implémentation de **IABProvider::Shutdown,** effectuez tout nettoyage final que vous pensez nécessaire. Par exemple, votre fournisseur peut appeler **MAPIDeinitIdle** s’il a appelé **MAPIInitIdle** pour utiliser le moteur inactif pendant la session ou la méthode **IUnknown::Release** des objets qui n’ont pas encore été publiés. 
  
Si votre fournisseur n’a pas de nettoyage final, son implémentation peut être composé d’une seule ligne de code : 
  
```cpp
return S_OK;

```


