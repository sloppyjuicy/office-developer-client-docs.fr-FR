---
title: Propriété canonique PidTagIconIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 83ab01363d478d197286bfa8f7b5b092a7ffd5a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786080"
---
# <a name="pidtagiconindex-canonical-property"></a>Propriété canonique PidTagIconIndex

  
  
**S’applique à**: Outlook 
  
Contient un nombre qui indique l’icône à utiliser lorsque vous affichez un groupe d’objets de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ICON_INDEX  <br/> |
|Identificateur :  <br/> |0x1080  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété, si elle existe, est un indicateur au client. Le client peut ignorer la valeur de cette propriété. 
  
|**Élément d’état de la messagerie**|**Index de l’icône**|
|:-----|:-----|
|Nouveau courrier  <br/> |0xFFFFFFFF  <br/> |
|Publication  <br/> |0x00000001  <br/> |
|Other  <br/> |0 x 00000003  <br/> |
|Lire le courrier  <br/> |0 x 00000100  <br/> |
|Courrier non lu  <br/> |0 x 00000101  <br/> |
|Courrier envoyé  <br/> |0x00000102  <br/> |
|Messages non envoyés  <br/> |0x00000103  <br/> |
|Messages d’accusé de réception  <br/> |0x00000104  <br/> |
|Messagerie de réponse  <br/> |0x00000105  <br/> |
|Courrier transféré  <br/> |0x00000106  <br/> |
|Courrier à distance  <br/> |0x00000107  <br/> |
|Messagerie de remise  <br/> |0x00000108  <br/> |
|Lire le courrier  <br/> |0x00000109  <br/> |
|Messagerie de non-remise  <br/> |0x0000010A  <br/> |
|Messagerie nonread  <br/> |0x0000010B  <br/> |
|Messagerie Recall_S  <br/> |0x0000010C  <br/> |
|Messagerie Recall_F  <br/> |0x0000010D  <br/> |
|Suivi des messages  <br/> |0x0000010E  <br/> |
|En dehors de la messagerie office  <br/> |0x0000011B  <br/> |
|Rappeler la messagerie  <br/> |0x0000011C  <br/> |
|Suivi des messages  <br/> |0x00000130  <br/> |
|Contact  <br/> |0 x 00000200  <br/> |
|Liste de distribution  <br/> |0x00000202  <br/> |
|Bleu pense-bête  <br/> |0x00000300  <br/> |
|Vert pense-bête  <br/> |0x00000301  <br/> |
|Rose pense-bête  <br/> |0x00000302  <br/> |
|Jaune pense-bête  <br/> |0x00000303  <br/> |
|Livre pense-bête  <br/> |0x00000304  <br/> |
|Rendez-vous unique  <br/> |0 x 00000400  <br/> |
|Rendez-vous périodique  <br/> |0x00000401  <br/> |
|Réunion unique  <br/> |0x00000402  <br/> |
|Réunion périodique  <br/> |0x00000403  <br/> |
|Demande de réunion  <br/> |0 x 00000404  <br/> |
|Accepter  <br/> |0x00000405  <br/> |
|Refuser  <br/> |0x00000406  <br/> |
|Tentativly  <br/> |0 x 00000407  <br/> |
|Annulation  <br/> |0x00000408  <br/> |
|Mise à jour d’information  <br/> |0 x 00000409  <br/> |
|/ Tâche  <br/> |0x00000500  <br/> |
|Tâche périodique non attribué  <br/> |0x00000501  <br/> |
|Tâche de la personne affectée  <br/> |0x00000502  <br/> |
|Tâche d’assigne  <br/> |0x00000503  <br/> |
|Demande de tâche  <br/> |0x00000504  <br/> |
|Acceptation de tâche  <br/> |0x00000505  <br/> |
|Refus de tâche  <br/> |0x00000506  <br/> |
|Conversation de journal  <br/> |0x00000601  <br/> |
|Message électronique de journal  <br/> |0x00000602  <br/> |
|Demande de réunion de journal  <br/> |0x00000603  <br/> |
|Réponse à une réunion journal  <br/> |0x00000604  <br/> |
|Demande de tâche de journal  <br/> |0x00000606  <br/> |
|Réponse de la tâche feuille  <br/> |0x00000607  <br/> |
|Note du journal  <br/> |0x00000608  <br/> |
|Télécopie de journal  <br/> |0x00000609  <br/> |
|Appel téléphonique de journal  <br/> |0x0000060A  <br/> |
|Lettre de journal  <br/> |0x0000060C  <br/> |
|Feuille Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Feuille Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Feuille Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Feuille Microsoft Office Access  <br/> |0x00000610  <br/> |
|Document de feuille  <br/> |0x00000612  <br/> |
|Réunion de journal  <br/> |0x00000613  <br/> |
|Annulation de réunion de journal  <br/> |0x00000614  <br/> |
|Session à distance de journal  <br/> |0x00000615  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les contacts et les listes de distribution personnelle.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

