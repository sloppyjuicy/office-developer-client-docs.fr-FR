---
title: Propriété canonique PidTagContainerContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392731"
---
# <a name="pidtagcontainercontents-canonical-property"></a>Propriété canonique PidTagContainerContents

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un objet incorporé contenu tableau qui fournit des informations relatives à un conteneur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_CONTENTS  <br/> |
|Identificateur :  <br/> |0x360F  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) . En tant que propriété de type PT_OBJECT, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande l’identificateur d’interface IID_IMAPITable. Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) s’il est défini, mais peut le signaler ou pas si elle n’est pas définie. 
  
Pour récupérer le contenu du tableau, une application cliente doit appeler la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) . For more information, see [Tables des mati�res](contents-tables.md). 
  
Cette propriété, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) et **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sont similaires d’utilisation. Plusieurs propriétés MAPI fournissent l’accès aux tables : 
  
|**Propriété**|**Table**|
|:-----|:-----|
|PidTagContainerContents  <br/> |Table des matières  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Table de hiérarchie  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tableau contenu associé  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Table des pièces jointes  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Table des destinataires  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

