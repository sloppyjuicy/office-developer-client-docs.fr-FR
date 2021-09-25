---
title: Propriété canonique PidTagContainerContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8471cbf985a758b07a4481942b2876b29ebb4c2c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575035"
---
# <a name="pidtagcontainercontents-canonical-property"></a>Propriété canonique PidTagContainerContents

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un objet de table de contenu incorporé qui fournit des informations sur un conteneur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_CONTENTS  <br/> |
|Identificateur :  <br/> |0x360F  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Conteneur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations [IMAPIProp::CopyProps.](imapiprop-copyprops.md) En tant que propriété de type PT_OBJECT, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) en demandant l’identificateur IID_IMAPITable’interface. Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peuvent éventuellement la signaler ou non si elle n’est pas définie. 
  
Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md) For more information, see [Tables des mati�res](contents-tables.md). 
  
Cette propriété, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) et **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sont similaires dans l’utilisation. Plusieurs propriétés MAPI permettent d’accéder aux tables : 
  
|**Propriété**|**Table**|
|:-----|:-----|
|PidTagContainerContents  <br/> |Table Contents  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Table Hierarchy  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Table des matières associée  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Table Attachment  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Table Recipient  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

