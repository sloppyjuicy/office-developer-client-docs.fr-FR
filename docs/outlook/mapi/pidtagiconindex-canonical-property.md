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
ms.openlocfilehash: 35d9d0a50539f8aab2d26730dd4e4544c2535e60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346619"
---
# <a name="pidtagiconindex-canonical-property"></a>Propriété canonique PidTagIconIndex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un nombre qui indique l'icône à utiliser lorsque vous affichez un groupe d'objets de courrier électronique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ICON_INDEX  <br/> |
|Identificateur :  <br/> |0x1080  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété, si elle existe, est une indication pour le client. Le client peut ignorer la valeur de cette propriété. 
  
|**État de l'élément de courrier**|**Index d'icône**|
|:-----|:-----|
|Nouveau message électronique  <br/> |Égale  <br/> |
|Publication  <br/> |0x00000001  <br/> |
|Autre  <br/> |0x00000003  <br/> |
|Lire le courrier  <br/> |0x00000100  <br/> |
|Courrier non lu  <br/> |0x00000101  <br/> |
|Messages envoyés  <br/> |0x00000102  <br/> |
|Courrier non envoyé  <br/> |0x00000103  <br/> |
|Courrier de réception  <br/> |0x00000104  <br/> |
|Courrier reçu  <br/> |0x00000105  <br/> |
|Courrier transféré  <br/> |0x00000106  <br/> |
|Courrier à distance  <br/> |0x00000107  <br/> |
|Courrier de remise  <br/> |0x00000108  <br/> |
|Lire le courrier  <br/> |0x00000109  <br/> |
|Courrier à livraison incomplète  <br/> |0x0000010A  <br/> |
|Courrier non lu  <br/> |0x0000010B  <br/> |
|Recall_S mail  <br/> |0x0000010C  <br/> |
|Recall_F mail  <br/> |0x0000010D  <br/> |
|Suivi du courrier électronique  <br/> |0x0000010E  <br/> |
|Courrier absent (e) du Bureau  <br/> |0x0000011B  <br/> |
|Rappeler le courrier  <br/> |0x0000011C  <br/> |
|Courrier suivi  <br/> |0x00000130  <br/> |
|Contact  <br/> |0x00000200  <br/> |
|Liste de distribution  <br/> |0x00000202  <br/> |
|Pense-bête bleu  <br/> |0x00000300  <br/> |
|Pense-bête en vert  <br/> |0x00000301  <br/> |
|Pense-bête rose  <br/> |0x00000302  <br/> |
|Pense-bête jaune  <br/> |0x00000303  <br/> |
|Pense-bête blanc  <br/> |0x00000304  <br/> |
|Rendez-vous unique  <br/> |0x00000400  <br/> |
|Rendez-vous périodique  <br/> |0x00000401  <br/> |
|Réunion d'instance unique  <br/> |0x00000402  <br/> |
|Réunion périodique  <br/> |0x00000403  <br/> |
|Demande de réunion  <br/> |0x00000404  <br/> |
|Accepter  <br/> |0x00000405  <br/> |
|Amortissement  <br/> |0x00000406  <br/> |
|Tentativly  <br/> |0x00000407  <br/> |
|Annulation  <br/> |0x00000408  <br/> |
|Mise à jour des informations  <br/> |0x00000409  <br/> |
|Tâche/tâche  <br/> |0x00000500  <br/> |
|Tâche périodique non affectée  <br/> |0x00000501  <br/> |
|Tâche de l'intervenant  <br/> |0x00000502  <br/> |
|Tâche de l'utilisateur  <br/> |0x00000503  <br/> |
|Demande de tâche  <br/> |0x00000504  <br/> |
|Acceptation de la tâche  <br/> |0x00000505  <br/> |
|Rejet de tâche  <br/> |0x00000506  <br/> |
|Conversation de journal  <br/> |0x00000601  <br/> |
|Message électronique de journal  <br/> |0x00000602  <br/> |
|Demande de réunion de journal  <br/> |0x00000603  <br/> |
|Réponse à une réunion de journal  <br/> |0x00000604  <br/> |
|Demande de tâche de journal  <br/> |0x00000606  <br/> |
|Réponse de tâche de journal  <br/> |0x00000607  <br/> |
|Note de journal  <br/> |0x00000608  <br/> |
|Télécopie de journal  <br/> |0x00000609  <br/> |
|Appel de journal téléphonique  <br/> |0x0000060A  <br/> |
|Lettre du journal  <br/> |0x0000060C  <br/> |
|Journal Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Journal Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Journal Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Journal Microsoft Office Access  <br/> |0x00000610  <br/> |
|Document de journal  <br/> |0x00000612  <br/> |
|Réunion de journal  <br/> |0x00000613  <br/> |
|Annulation de réunion de journal  <br/> |0x00000614  <br/> |
|Session à distance de journal  <br/> |0x00000615  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

