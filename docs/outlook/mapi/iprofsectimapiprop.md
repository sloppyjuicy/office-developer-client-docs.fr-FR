---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3046e8e71af92015ca5fd40e8a81c2afa8db89ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571569"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fonctionne avec les propriétés des objets de section de profil. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Exposé par :  <br/> |Objets de section de profil  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IProfSect  <br/> |
|Type de pointeur :  <br/> |LPPROFSECT  <br/> |
|Modèle de transaction :  <br/> |Non traduit  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

Cette interface n’a pas de méthode unique.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="notes-to-callers"></a>Remarques pour les appelants

**L’interface IProfSect** ne possède aucune méthode unique, mais vous pouvez appeler les méthodes [IMAPIProp](imapipropiunknown.md) de la section de profil. Il existe certaines différences entre l’implémentation **IProfSect** et d’autres implémentations **d’IMAPIProp**:
  
- **IProfSect ne** prend pas en charge un modèle de transaction. 
    
- **IProfSect ne** prend pas en charge les propriétés nommées. 
    
- **IProfSect** réserve la plage d’identificateurs 0x67F0 à 0x67ff pour les propriétés sécurisées. 
    
La non-prise en charge d’un modèle de transaction signifie que toutes les modifications apportées à une section de profil à la suite d’appels aux méthodes [IMAPIProp::CopyProps](imapiprop-copyprops.md) et [IMAPIProp::CopyTo](imapiprop-copyto.md) se produisent immédiatement. Les appels à [la méthode IMAPIProp::SaveChanges](imapiprop-savechanges.md) réussissent, mais n’enregistrent pas réellement les modifications. 
  
Pour être protégés contre les modifications qui se produisent prématurément, les fournisseurs de services doivent effectuer des copies de leurs sections de profil qui sont affichées aux utilisateurs par le biais de feuilles de propriétés. Les feuilles de propriétés doivent fonctionner avec la copie, au lieu de la section de profil réelle. Lorsque l’utilisateur clique sur le bouton **OK** pour vérifier que les modifications sont exactes, les modifications peuvent être enregistrées dans la section profil réel. 
  
Pour implémenter une feuille de propriétés à l’aide d’une section de profil copiée, utilisez la procédure suivante :
  
1. Ouvrez la section profil en appelant la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md) 
    
2. Appelez la [fonction CreateIProp](createiprop.md) pour récupérer un objet de données de propriété , un objet qui prend en charge l’interface **IPropData.** 
    
3. Appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) de la section de profil pour copier les propriétés qui apparaîtront dans la feuille des propriétés de la section profil vers l’objet de données de propriété. 
    
4. Appelez la méthode [IMAPISupport::D oConfigPropSheet](imapisupport-doconfigpropsheet.md) pour demander au fournisseur de services d’afficher une feuille de propriétés et passez un pointeur vers l’objet de données de propriété dans le paramètre _lpConfigData._ 
    
5. Lorsque l’utilisateur enregistre les modifications apportées aux propriétés de configuration dans la feuille des propriétés, appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) pour copier les propriétés de l’objet de données de propriété dans la section de profil. 
    
Les sections de profil, contrairement aux autres objets, ne sont pas en charge les propriétés nommées. Les méthodes [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) retournent MAPI_E_NO_SUPPORT si elles sont appelées sur un objet de section de profil. Si vous utilisez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir les identificateurs de propriété dans la plage ci-dessus 0x8000, le type de propriété PT_ERROR est renvoyé. 
  
Les sections de profil réservent la plage d'0x67F0 à 0x67FF pour les propriétés sécurisées. Les fournisseurs de services peuvent utiliser cette plage pour stocker des mots de passe et d’autres informations d’identification spécifiques au fournisseur. Les propriétés de cette plage ne sont pas renvoyées dans la liste complète des propriétés lorsque NULL est transmis dans le paramètre _lpPropTag_ de la méthode [IMAPIProp::GetProps,](imapiprop-getprops.md) ni dans le paramètre _lppPropTagArray_ de la méthode [IMAPIProp::GetPropList.](imapiprop-getproplist.md) Les propriétés sécurisées doivent être demandées spécifiquement par leurs identificateurs. 
  
MAPI fournit une section de profil avec la constante codée en dur MUID_PROFILE_INSTANCE comme identificateur et PR_SEARCH_KEY **(** [PidTagSearchKey](pidtagsearchkey-canonical-property.md)) comme propriété unique. MAPI garantit que la **valeur PR_SEARCH_KEY** propriété sera unique parmi tous les profils créés. Utilisez **PR_SEARCH_KEY** au lieu  de PR_PROFILE_NAME lorsque l’unicité est importante, car il est possible qu’un profil supprimé soit suivi d’un autre profil du même nom. 
  
Pour plus d’informations sur l’utilisation des sections de profil, voir [Administering Profiles and Message Services](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

