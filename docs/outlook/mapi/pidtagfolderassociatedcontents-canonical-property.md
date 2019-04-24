---
title: Propriété canonique PidTagFolderAssociatedContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316302"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a>Propriété canonique PidTagFolderAssociatedContents

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un objet table de contenu incorporé qui fournit des informations sur le tableau des contenus associés. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLDER_ASSOCIATED_CONTENTS  <br/> |
|Identificateur :  <br/> |0x3610  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau contenu associé représente un sous-dossier qui n'apparaît pas dans la table des matières standard. Il contient les messages associés ou masqués du dossier. 
  
Cette propriété peut être exclue dans [IMAPIProp:: CopyTo](imapiprop-copyto.md) Operations ou incluse dans [IMAPIProp:: CopyProps](imapiprop-copyprops.md) Operations. En tant que propriété de type **PT_OBJECT**, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) ; son contenu doit être accessible à l'aide de la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , qui demande l'identificateur d'interface **IID_IMAPITable** . Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) s'il est défini, mais éventuellement le signaler ou non s'il n'est pas défini. 
  
Pour récupérer le contenu de la table, les applications clientes doivent appeler la méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) . Pour plus d'informations sur les tableaux de contenu de dossier, consultez la rubrique [content tables](contents-tables.md) and [affichant a folder content table](displaying-a-folder-contents-table.md). 
  
Les **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) et cette propriété sont similaires dans l'utilisation. Plusieurs propriétés MAPI permettent d'accéder à des tables: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Table des matières  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Table Hierarchy  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** <br/> |Table des matières associées  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Table des pièces jointes  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Table de destinataires  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l'ordre et le flux de transfert de données entre un client et un serveur.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les éléments de rendez-vous et de réunion.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

