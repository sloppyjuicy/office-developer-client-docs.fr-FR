---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344792"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fonctionne avec les propriétés des objets de section de profil. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix. h  <br/> |
|Exposé par:  <br/> |Objets de section de profil  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Identificateur de l'interface:  <br/> |IID_IProfSect  <br/> |
|Type de pointeur:  <br/> |LPPROFSECT  <br/> |
|Modèle de transaction:  <br/> |Pas de transaction  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

Cette interface n'a pas de méthodes uniques.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="notes-to-callers"></a>Remarques pour les appelants

L'interface **IProfSect** ne possède pas de méthodes uniques, mais vous pouvez appeler les méthodes [IMAPIProp](imapipropiunknown.md) de la section profil. Il existe certaines différences entre l'implémentation de **IProfSect** et d'autres implémentations de **IMAPIProp**:
  
- **IProfSect** ne prend pas en charge un modèle de transaction. 
    
- **IProfSect** ne prend pas en charge les propriétés nommées. 
    
- **IProfSect** réserve la plage d'identificateurs 0x67F0 à 0x67ff pour les propriétés sécurisées. 
    
Ne pas prendre en charge un modèle de transaction signifie que toutes les modifications apportées à une section de profil suite aux appels aux méthodes [IMAPIProp:: CopyProps](imapiprop-copyprops.md) et [IMAPIProp:: CopyTo](imapiprop-copyto.md) se produisent immédiatement. Les appels à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) réussissent sans enregistrer les modifications. 
  
Pour être protégé contre les modifications qui se produisent prématurément, les fournisseurs de services doivent faire des copies de leurs sections de profil affichées aux utilisateurs par le biais de feuilles de propriétés. Les feuilles de propriétés doivent fonctionner avec la copie, au lieu de la section Profil réel. Lorsque l'utilisateur clique sur le bouton **OK** pour vérifier que les modifications sont exactes, celles-ci peuvent être enregistrées dans la section Profil réel. 
  
Pour implémenter une feuille de propriétés à l'aide d'une section de profil copiée, procédez comme suit:
  
1. Ouvrez la section profil en appelant la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) ou [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) . 
    
2. Appelez la fonction [CreateIProp](createiprop.md) pour récupérer un objet de données de propriété, un objet qui prend en charge l'interface **IPropData** . 
    
3. Appelez la méthode [IMAPIProp:: CopyTo](imapiprop-copyto.md) de la section Profil pour copier les propriétés qui apparaîtront sur la feuille de propriétés à partir de la section Profil vers l'objet de données de propriété. 
    
4. Appelez la méthode [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) pour demander à ce que le fournisseur de services affiche une feuille de propriétés, puis transmettez un pointeur à l'objet de données de la propriété dans le paramètre _lpConfigData_ . 
    
5. Lorsque l'utilisateur enregistre les modifications apportées aux propriétés de configuration dans la feuille des propriétés, appelez la méthode [IMAPIProp:: CopyTo](imapiprop-copyto.md) pour copier les propriétés de l'objet de données de la propriété dans la section profil. 
    
Les sections de profil, contrairement à d'autres objets, ne prennent pas en charge les propriétés nommées. Les méthodes [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp:: GETNAMESFROMIDS](imapiprop-getnamesfromids.md) renvoient MAPI_E_NO_SUPPORT si elles sont appelées sur un objet de section de profil. Si vous utilisez la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) pour définir des identificateurs de propriété dans la plage au-dessus de 0x8000, le type de propriété PT_ERROR sera retourné. 
  
Les sections de profil réservent la plage d'identificateur 0x67F0 à 0x67FF pour les propriétés sécurisées. Les fournisseurs de services peuvent utiliser cette plage pour stocker les mots de passe et d'autres informations d'identification propres au fournisseur. Les propriétés de cette plage ne sont pas renvoyées dans la liste complète des propriétés lorsque la valeur NULL est transmise dans le paramètre _lpPropTag_ de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) , et non dans le paramètre _lppPropTagArray_ de l' [énumération Méthode IMAPIProp:: GetPropList](imapiprop-getproplist.md) . Les propriétés sécurisées doivent être demandées spécifiquement par leurs identificateurs. 
  
MAPI fournit une section de profil avec la constante codée en dur MUID_PROFILE_INSTANCE en tant qu'identificateur et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) comme propriété unique. MAPI garantit que la valeur de la propriété **PR_SEARCH_KEY** sera unique parmi tous les profils créés. Utilisez **PR_SEARCH_KEY** au lieu de **PR_PROFILE_NAME** lorsque l'unicité est importante, car il est possible qu'un profil supprimé soit suivi par un autre profil portant le même nom. 
  
Pour plus d'informations sur l'utilisation des sections de profil, consultez la rubrique adMinistering Profiles [and message services](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

