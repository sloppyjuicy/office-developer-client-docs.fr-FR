---
title: IProfSect IMAPIProp
description: Décrit les propriétés et l’ordre de tableau virtuel des propriétés requises pour IProfSect IMAPIProp, qui fonctionne avec les propriétés des objets de section de profil.
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
ms.openlocfilehash: 8a2b062d990a80cfd0644c1a8b0cb2241f3f1861
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828359"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fonctionne avec les propriétés des objets de section de profil. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Exposé par :  <br/> |Objets de section de profil  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IProfSect  <br/> |
|Type de pointeur :  <br/> |LPPROFSECT  <br/> |
|Modèle de transaction :  <br/> |Non transactionnel  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

Cette interface n’a pas de méthodes uniques.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="notes-to-callers"></a>Remarques pour les appelants

L’interface **IProfSect** n’a pas de méthodes uniques, mais vous pouvez appeler les méthodes [IMAPIProp](imapipropiunknown.md) de la section de profil. Il existe quelques différences entre l’implémentation **IProfSect** et d’autres implémentations **d’IMAPIProp** :
  
- **IProfSect** ne prend pas en charge un modèle de transaction. 
    
- **IProfSect** ne prend pas en charge les propriétés nommées. 
    
- **IProfSect** réserve la plage d’identificateurs 0x67F0 à 0x67ff pour les propriétés sécurisées. 
    
Le fait de ne pas prendre en charge un modèle de transaction signifie que toutes les modifications apportées à une section de profil après les appels aux méthodes [IMAPIProp::CopyProps](imapiprop-copyprops.md) et [IMAPIProp::CopyTo](imapiprop-copyto.md) se produisent immédiatement. Les appels à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) réussissent, mais n’enregistrent pas réellement les modifications. 
  
Pour être protégés contre les modifications qui se produisent prématurément, les fournisseurs de services doivent effectuer des copies de leurs sections de profil qui sont affichées aux utilisateurs via des feuilles de propriétés. Les feuilles de propriétés doivent fonctionner avec la copie, au lieu de la section de profil réel. Lorsque l’utilisateur clique sur le bouton **OK** pour vérifier que les modifications sont exactes, les modifications peuvent être enregistrées dans la section profil réel. 
  
Pour implémenter une feuille de propriétés à l’aide d’une section de profil copiée, procédez comme suit :
  
1. Ouvrez la section profil en appelant la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . 
    
2. Appelez la fonction [CreateIProp](createiprop.md) pour récupérer un objet de données de propriété , un objet qui prend en charge l’interface **IPropData** . 
    
3. Appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) de la section profil pour copier les propriétés qui apparaîtront dans la feuille de propriétés de la section profil vers l’objet de données de propriété. 
    
4. Appelez la méthode [IMAPISupport::D oConfigPropSheet](imapisupport-doconfigpropsheet.md) pour demander au fournisseur de services d’afficher une feuille de propriétés et de passer un pointeur vers l’objet de données de propriété dans le paramètre _lpConfigData_ . 
    
5. Lorsque l’utilisateur enregistre les modifications apportées aux propriétés de configuration dans la feuille de propriétés, appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) pour copier les propriétés de l’objet de données de propriété vers la section profil. 
    
Contrairement aux autres objets, les sections de profil ne prennent pas en charge les propriétés nommées. Les méthodes [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) retournent MAPI_E_NO_SUPPORT si elles sont appelées sur un objet de section de profil. Si vous utilisez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir des identificateurs de propriété dans la plage ci-dessus 0x8000, le type de propriété PT_ERROR est retourné. 
  
Les sections de profil réservent la plage d’identificateurs 0x67F0 à 0x67FF pour les propriétés sécurisées. Les fournisseurs de services peuvent utiliser cette plage pour stocker des mots de passe et d’autres informations d’identification spécifiques au fournisseur. Les propriétés de cette plage ne sont pas retournées dans la liste complète des propriétés lorsque null est passé dans le paramètre _lpPropTag_ de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) , ni dans le paramètre _lppPropTagArray_ de la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) . Les propriétés sécurisées doivent être demandées spécifiquement par leurs identificateurs. 
  
MAPI fournit une section de profil avec la constante codée en dur MUID_PROFILE_INSTANCE comme identificateur et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) comme propriété unique. MAPI garantit que la valeur **de propriété PR_SEARCH_KEY** sera unique parmi tous les profils créés. Utilisez **PR_SEARCH_KEY** au lieu de **PR_PROFILE_NAME** lorsque l’unicité est importante, car il est possible qu’un profil supprimé soit suivi d’un autre profil portant le même nom. 
  
Pour plus d’informations sur l’utilisation des sections de profil, consultez [Administration des profils et des services de messages](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

