---
title: Propriété canonique PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9656af44d07f59b11d69b35b0c1b22bd8cdae349
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524282"
---
# <a name="pidtagmessagerecipients-canonical-property"></a>Propriété canonique PidTagMessageRecipients

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une table des restrictions qui peuvent être appliquées à une table des matières pour rechercher tous les messages qui contiennent des sous-objets de destinataire qui répondent aux restrictions. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_RECIPIENTS  <br/> |
|Identificateur :  <br/> |0x0E12  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations [IMAPIProp::CopyProps](imapiprop-copyprops.md) . En tant que propriété de type **PT_OBJECT**, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , demandant l’identificateur **IID_IMAPITable’interface** . Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peuvent éventuellement la signaler ou non si elle n’est pas définie. 
  
Pour récupérer le contenu de la table, une application cliente doit appeler la [méthode IMessage::GetRecipientTable](imessage-getrecipienttable.md) . 
  
Cette propriété peut être utilisée pour la restriction de sous-objet en la spécifiant dans la structure [SSubRestriction](ssubrestriction.md) . Cela permet à un client de limiter l’affichage d’un conteneur aux messages dont les destinataires réunionnt des critères donnés. Un message est éligible pour l’affichage si au moins une ligne dans la table des destinataires, c’est-à-dire qu’un destinataire satisfait à la restriction de sous-objet. 
  
 **Remarque** L’utilisation des résultats de restriction de sous-objet est l’équivalent d’un appel [IMAPISession::OpenEntry](imapisession-openentry.md) sur chaque message de la table. Selon l’application cliente et le nombre de messages à rechercher, cela peut affecter les performances. 
  
La **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) et cette propriété sont similaires dans l’utilisation. Plusieurs propriétés MAPI permettent d’accéder aux tables : 
  
|**Propriété**|**Tableau**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Table Contents  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Table Hierarchy  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Table des matières associée  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Table Attachment  <br/> |
|PR_MESSAGE_RECIPIENTS  <br/> |Table Recipient  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux des transferts de données entre un client et un serveur.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes d’adresses de courriers indésirables et la détermination des messages électroniques indésirables.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
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

