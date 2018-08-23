---
title: Propriété canonique PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6d0d2c07355140e89ffb24095d1ca3a302f6e5ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568447"
---
# <a name="pidtagmessagerecipients-canonical-property"></a>Propriété canonique PidTagMessageRecipients

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de restrictions qui peuvent être appliquées à une table des matières pour rechercher tous les messages qui contiennent des destinataires sous-objets répondant aux restrictions. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_RECIPIENTS  <br/> |
|Identificateur :  <br/> |0x0E12  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) . En tant que propriété de type **PT_OBJECT**, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande l’identificateur d’interface **IID_IMAPITable** . Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peut le signaler ou pas si elle n’est pas définie. 
  
Pour récupérer le contenu du tableau, une application cliente doit appeler la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) . 
  
Cette propriété peut être utilisée pour la restriction sous-objet en le définissant dans la structure [SSubRestriction](ssubrestriction.md) . Cela permet à un client limiter l’affichage d’un conteneur pour les messages avec des destinataires de réunion critère donné. Un message satisfait aux conditions requises pour l’affichage si la restriction sous-objet satisfait au moins une ligne dans sa table destinataire, c'est-à-dire, un seul destinataire. 
  
 **Remarque** Utilisation des résultats de restriction sous-objet est l’équivalent d’une [IMAPISession::OpenEntry](imapisession-openentry.md) des appels sur chaque message dans le tableau. En fonction de l’application cliente et le nombre de messages à rechercher, il peut affecter les performances. 
  
La propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) et cette propriété sont similaires d’utilisation. Plusieurs propriétés MAPI fournissent l’accès aux tables : 
  
|**Propriété**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Table des matières  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Table de hiérarchie  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tableau contenu associé  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Table des pièces jointes  <br/> |
|PR_MESSAGE_RECIPIENTS  <br/> |Table des destinataires  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
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

