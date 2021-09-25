---
title: Propriété canonique PidTagLastVerbExecuted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagLastVerbExecuted
api_type:
- HeaderDef
ms.assetid: 502f0261-697f-41bf-8530-75e1d0f503e5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4e5e13f54cf33542ac8a73a28e5cfb948e484dba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587537"
---
# <a name="pidtaglastverbexecuted-canonical-property"></a>Propriété canonique PidTagLastVerbExecuted

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le dernier verbe exécuté.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LAST_VERB_EXECUTED  <br/> |
|Identificateur :  <br/> |0x1081  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Historique  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir l’une des valeurs suivantes :
  
|**Verb**|**Valeur de la propriété**|
|:-----|:-----|
|Publication  <br/> |0x00000001  <br/> |
|Autres  <br/> |0x00000003  <br/> |
|Lire le courrier électronique  <br/> |0x00000100  <br/> |
|Courrier non lu  <br/> |0x00000101  <br/> |
|Courrier envoyé  <br/> |0x00000102  <br/> |
|Courrier non envoyé  <br/> |0x00000103  <br/> |
|Accusé de réception  <br/> |0x00000104  <br/> |
|Courriers électroniques répondus  <br/> |0x00000105  <br/> |
|Courrier électronique transmis  <br/> |0x00000106  <br/> |
|Courrier distant  <br/> |0x00000107  <br/> |
|Accusé de réception  <br/> |0x00000108  <br/> |
|Accusé de lecture  <br/> |0x00000109  <br/> |
|Reçu nondelivery  <br/> |0x0000010A  <br/> |
|Reçu non lu  <br/> |0x0000010B  <br/> |
|Recall_S courrier électronique  <br/> |0x0000010C  <br/> |
|Recall_F courrier électronique  <br/> |0x0000010D  <br/> |
|Suivi du courrier électronique  <br/> |0x0000010E  <br/> |
|Courrier électronique Office courrier électronique non envoyé  <br/> |0x0000011B  <br/> |
|Rappeler le courrier  <br/> |0x0000011C  <br/> |
|Courrier suivi  <br/> |0x00000139  <br/> |
|Contact  <br/> |0x00000200  <br/> |
|Liste de distribution  <br/> |0x00000201  <br/> |
|Note rouge, Bleu  <br/> |0x00000300  <br/> |
|Note sticky, vert  <br/> |0x00000301  <br/> |
|Note ressoyante, rose  <br/> |0x00000302  <br/> |
|Note rouge, jaune  <br/> |0x00000303  <br/> |
|Note rouge, blanc  <br/> |0x00000304  <br/> |
|Rendez-vous à instance unique  <br/> |0x00000400  <br/> |
|Rendez-vous périodique  <br/> |0x00000401  <br/> |
|Réunion à instance unique  <br/> |0x00000402  <br/> |
|Réunion périodique  <br/> |0x00000403  <br/> |
|Demande de réunion / Mise à jour complète  <br/> |0x00000404  <br/> |
|Accepter  <br/> |0x00000405  <br/> |
|Refuser  <br/> |0x00000406  <br/> |
|Accepter provisoirement  <br/> |0x00000407  <br/> |
|Annulation  <br/> |0x00000408  <br/> |
|Mise à jour d’informations  <br/> |0x00000409  <br/> |
|Mise à jour de tâche/tâche  <br/> |0x00000500  <br/> |
|Tâche périodique non assignée  <br/> |0x00000501  <br/> |
|Tâche de l’affectation  <br/> |0x00000502  <br/> |
|Tâche de l’assigneur  <br/> |0x00000503  <br/> |
|Demande de tâche  <br/> |0x00000504  <br/> |
|Acceptation des tâches  <br/> |0x00000505  <br/> |
|Rejet de tâche  <br/> |0x00000506  <br/> |
|Journal Conversation  <br/> |0x00000601  <br/> |
|Message électronique de journal  <br/> |0x00000602  <br/> |
|Demande de réunion de journal  <br/> |0x00000603  <br/> |
|Réponse à une réunion de journal  <br/> |0x00000604  <br/> |
|Demande de tâche de journal  <br/> |0x00000606  <br/> |
|Réponse de la tâche de journal  <br/> |0x00000607  <br/> |
|Journal Note  <br/> |0x00000608  <br/> |
|Télécopie de journal  <br/> |0x00000609  <br/> |
|Appel de journal Téléphone journal  <br/> |0x0000060A  <br/> |
|Tâche de journal  <br/> |0x0000060B  <br/> |
|Lettre de journal  <br/> |0x0000060C  <br/> |
|Journal Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Journal Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Journal Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Accès Microsoft Office journal  <br/> |0x00000610  <br/> |
|Journal Document  <br/> |0x00000612  <br/> |
|Journal Meeting  <br/> |0x00000613  <br/> |
|Annulation d’une réunion de journal  <br/> |0x00000614  <br/> |
|Session journal à distance  <br/> |0x00000615  <br/> |
|Nouveau courrier  <br/> |0xFFFFFFFF  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> 
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

