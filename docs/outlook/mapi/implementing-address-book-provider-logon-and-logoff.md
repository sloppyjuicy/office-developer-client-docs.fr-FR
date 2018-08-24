---
title: Implémentation d’ouverture et de fermeture de session de fournisseur de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f26e7b7ec607c9714012870d5367a0e775c62f34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572101"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implémentation d’ouverture et de fermeture de session de fournisseur de carnet d’adresses

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournisseurs de carnet d’adresses en charge d’ouverture de session et de fermeture de session en implémentant les méthodes de le [IABProvider : IUnknown](iabprovideriunknown.md) interface. Le ** IABProvider ** interface hérite directement à partir de **IUnknown** et ajoute deux autres méthodes : **ouverture de session** et **d’arrêt**. 
  
## <a name="logoff"></a>Logoff

MAPI appelle votre méthode de fournisseur [IABProvider::Logon](iabprovider-logon.md) au début de chaque session et chaque fois que votre fournisseur est ajouté au profil actif et le client prend en charge la reconfiguration dynamique. Lorsque la méthode **IABProvider::Logon** appels MAPI, votre fournisseur de carnet d’adresses commence son processus d’ouverture de session. 
  
**Pour mettre en œuvre IABProvider::Log**
  
1. Initialiser tous les pointeurs de paramètre de sortie passés par MAPI. 
    
2. Appeler la méthode **IUnknown::AddRef** de l’objet de la prise en charge pour incrémenter son décompte de références. 
    
3. Appeler la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) de l’objet de la prise en charge pour ouvrir la section du profil qui contient les informations de configuration de votre fournisseur. Passez la valeur NULL pour le paramètre _lpUID_ et l’indicateur ne si vous souhaitez apporter des modifications. 
    
4. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la section profil pour récupérer les propriétés qui ont besoin de votre fournisseur d’ouverture de session, telles que le nom de la table de base de données ou du fichier de données. 
    
5. Vérifiez que les propriétés sont tous disponibles et valide. Si nécessaire et autorisés, afficher une boîte de dialogue pour inviter l’utilisateur d’effectuer des corrections ou des ajouts aux informations non valides ou absente et appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la section profil pour enregistrer les modifications. Les propriétés communes qui doivent être disponibles sont les suivantes : 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Ne définissez pas **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). Au moment de l’ouverture de session, ces propriétés sont en lecture seule. 
  
6. Si une ou plusieurs propriétés de configuration ne sont pas disponibles, échouer et retourner la valeur MAPI_E_UNCONFIGURED.
    
7. Appelez [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire un [MAPIUID](mapiuid.md). Votre fournisseur peut créer un **MAPIUID** par : 
    
   - L’appel de la méthode [IMAPISupport::NewUID](imapisupport-newuid.md) . 
    
   - L’appel de la UUIDGEN. Outil EXE pour définir un GUID utilisé par votre fournisseur à inclure dans un des fichiers d’en-tête.
    
8. Si vous le souhaitez, enregistrer un nouveau **MAPIUID** dans le profil actif en appelant la section profil ** IMAPIProp::SetProps ** méthode. 
    
9. Version de la section profil en appelant la méthode **IUnknown::Release** . 
    
10. Instanciez un nouvel objet d’ouverture de session et définir le contenu du paramètre _lppABLogon_ à l’adresse de ce nouvel objet. 
    
Puisqu’il est possible de MAPI appeler votre ** ouverture de session ** méthode plusieurs fois au cours d’une session, nous vous conseillons prendre en charge cette possibilité dans votre implémentation lorsqu’ils sont en mesure de créer plusieurs objets d’ouverture de session et garder une trace de chaque objet est créé. Prise en charge de plusieurs appels **d’ouverture de session** permet à un utilisateur d’une application cliente, par exemple, pour vous connecter à une session avec différentes identités ou utiliser livraison différentes destinations. 
  
**L’arrêt** est appelée lorsque la session se termine. MAPI appelle votre méthode [IABProvider::Shutdown](iabprovider-shutdown.md) comme une des tâches dernières impliquées dans la fermeture d’une session. MAPI a publié tous les objets de connexion de votre fournisseur et, lorsque votre fournisseur reçoit cet appel, il peut supposer qu’il s’agit du dernier appel qu’il reçoit. Dans votre implémentation de **IABProvider::Shutdown**, effectuez un nettoyage final que vous estimez est nécessaire. Par exemple, votre fournisseur peut appeler **MAPIDeinitIdle** s’il a appelé **MAPIInitIdle** pour utiliser le moteur inactif pendant la session ou de la méthode **IUnknown::Release** de tous les objets qui n’ont pas encore libérée. 
  
Si votre fournisseur n’a aucun nettoyage final, son implémentation peut être constituée d’une seule ligne de code : 
  
```cpp
return S_OK;

```


