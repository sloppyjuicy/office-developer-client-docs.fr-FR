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
ms.openlocfilehash: c0653caec5f3cac531206e1bb9c4330cac5f3133
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784404"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**S’applique à**: Outlook 
  
Fonctionne avec les propriétés des objets de section de profil. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Exposés par :  <br/> |Objets de section de profil  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
|Identificateur de l’interface :  <br/> |IID_IProfSect  <br/> |
|Type de pointeur :  <br/> |LPPROFSECT  <br/> |
|Modèle de transaction :  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

Cette interface n’a pas de méthodes uniques.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="notes-to-callers"></a>Notes aux appelants

L’interface **IProfSect** n’a pas de méthodes uniques qui lui est propre, mais vous pouvez appeler le profil de méthodes [IMAPIProp](imapipropiunknown.md) de la section. Il existe certaines différences entre l’implémentation de **IProfSect** et d’autres implémentations de **IMAPIProp**:
  
- **IProfSect** ne prend pas en charge un modèle de transaction. 
    
- **IProfSect** ne prend pas en charge propriétés nommées. 
    
- **IProfSect** réserve de la plage d’identificateurs 0x67F0 à 0x67ff pour les propriétés d’informations sécurisé. 
    
Ne prend ne pas en charge un modèle de transaction signifie que toutes les modifications qui ont été apportées à un suivante de la section profil des appels à l' [IMAPIProp::CopyProps](imapiprop-copyprops.md) et méthodes [IMAPIProp::CopyTo](imapiprop-copyto.md) se produisent immédiatement. Les appels à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) réussissent, mais n’enregistrement pas réellement de toutes les modifications. 
  
Pour être protégé contre les modifications qui se produisent prématurément, fournisseurs de services besoin d’effectuer des copies de leurs sections profil affichées aux utilisateurs par le biais de feuilles de propriétés. Les feuilles de propriétés devraient fonctionner avec la copie, au lieu de la section profil réel. Lorsque l’utilisateur clique sur le bouton **OK** pour vous assurer que les modifications sont correctes, les modifications peuvent être enregistrées dans la section profil réel. 
  
Pour implémenter une feuille de propriétés à l’aide d’une section de profil copié, utilisez la procédure suivante :
  
1. Ouvrez la section profil en appelant la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . 
    
2. Appelez la fonction [CreateIProp](createiprop.md) pour récupérer un objet de données de propriété, un objet qui prend en charge l’interface **IPropData** . 
    
3. Appeler la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) de la section profil pour copier les propriétés qui seront affiche sur la feuille des propriétés de la section de profil à l’objet de données de propriété. 
    
4. Appelez la méthode [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) pour demander que le fournisseur de services afficher une feuille de propriétés et passer un pointeur vers l’objet de données de propriété dans le paramètre _lpConfigData_ . 
    
5. Lorsque l’utilisateur enregistre les modifications apportées aux propriétés de configuration dans la feuille des propriétés, appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) pour copier les propriétés de l’objet de données de propriété à la section de profil. 
    
Sections, contrairement aux autres objets de profil, ne prennent pas en charge les propriétés nommées. Les méthodes [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) retournent MAPI_E_NO_SUPPORT si elles sont appelées sur un objet de section de profil. Si vous utilisez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir les identificateurs de propriété dans la plage supérieure à 0 x 8000, le type de propriété PT_ERROR est retourné. 
  
Sections profil réservent la plage d’identificateurs 0x67F0 à 0x67FF pour les propriétés d’informations sécurisé. Fournisseurs de services peuvent utiliser cette plage pour stocker les mots de passe et autres informations d’identification spécifiques au fournisseur. Propriétés de cette plage ne sont pas renvoyées dans la liste complète des propriétés lorsque NULL est indiqué dans le paramètre _lpPropTag_ de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) , ni qu’ils sont retournés dans le paramètre _lppPropTagArray_ de le [ IMAPIProp::GetPropList](imapiprop-getproplist.md) méthode. Propriétés sécurisées doivent être demandées explicitement par leurs identificateurs. 
  
MAPI fournit une section de profil avec le MUID_PROFILE_INSTANCE constante codé en dur son identificateur et **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) en tant que sa propriété unique. MAPI garantit que la valeur de la propriété **clé PR_SEARCH_KEY** unique parmi tous les profils créés. Utilisez **clé PR_SEARCH_KEY** au lieu de **PR_PROFILE_NAME** si l’unicité est importante, car il est possible pour un profil supprimé être suivie d’un autre profil portant le même nom. 
  
Pour plus d’informations sur l’utilisation des sections de profil, voir [administration des profils et des Services de messagerie](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

