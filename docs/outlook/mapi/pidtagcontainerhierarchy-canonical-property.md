---
title: Propriété canonique PidTagContainerHierarchy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332857"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a>Propriété canonique PidTagContainerHierarchy

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un objet table de hiérarchie incorporé qui fournit des informations sur les conteneurs enfants. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_HIERARCHY  <br/> |
|Identificateur :  <br/> |0x360E  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations [IMAPIProp::CopyProps.](imapiprop-copyprops.md) En tant que propriété de type **PT_OBJECT**, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) en demandant l’identificateur IID_IMAPITable’interface. Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peuvent éventuellement la signaler ou non si elle n’est pas définie. 
  
Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMAPIContainer::GetHierarchyTable.](imapicontainer-gethierarchytable.md) Pour plus d’informations, [voir Tables de hiérarchie.](hierarchy-tables.md) 
  
 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) et cette propriété sont similaires dans l’utilisation. Plusieurs propriétés MAPI permettent d’accéder aux tables : 
  
|**Propriété**|**Tableau**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Table Contents  <br/> |
|**PR_CONTAINER_HIERARCHY** <br/> |Table Hierarchy  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Table des matières associée  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Table Attachment  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Table Recipient  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux des transferts de données entre un client et un serveur.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.
    
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

