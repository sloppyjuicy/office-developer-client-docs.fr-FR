---
title: Affichage des lignes et des colonnes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ee60e64559a0b4163074ddb62ed72c4600c8e03d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783191"
---
# <a name="displaying-table-rows-and-columns"></a>Affichage des lignes et des colonnes

  
  
**S’applique à**: Outlook 
  
 Une page de propriétés peut être utilisée par un fournisseur de carnet d’adresses pour permettre aux utilisateurs de définir les destinataires du courrier électronique. 
  
Le tableau d’affichage correspondant comporte quatre lignes, un pour chaque contrôle. Les valeurs pour les colonnes qui indiquent la position sont comme suit.
  
|**Contrôle**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|Étiquette de nom d’affichage  <br/> |14  <br/> |18  <br/> |49  <br/> |8  <br/> |
|Zone de modification du nom complet  <br/> |76  <br/> |16  <br/> |89  <br/> |12  <br/> |
|Étiquette d’adresse de messagerie  <br/> |14  <br/> |42  <br/> |50  <br/> |8  <br/> |
|Zone d’édition d’adresse de messagerie  <br/> |76  <br/> |40  <br/> |89  <br/> |12  <br/> |
|Case à cocher  <br/> |14  <br/> |64  <br/> |90  <br/> |12  <br/> |
   
Le tableau suivant indique les valeurs appropriées pour le type de contrôle, sa propriété **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) et un masque de bits d’indicateurs, sa propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
  
|**Contrôle**|**Type**|**Flags**|
|:-----|:-----|:-----|
|Étiquette de nom d’affichage  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Zone de modification du nom complet  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Étiquette d’adresse de messagerie  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Zone d’édition d’adresse de messagerie  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Case à cocher  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
La table finale répertorie chaque contrôle avec le contenu de la structure de contrôle associé. Notez que la valeur pour chacun des contrôles label s’affiche dans la mémoire juste après la structure.
  
|**Contrôle**|**Structure**|
|:-----|:-----|
|Étiquette de nom d’affichage  <br/> |{0 sizeof(DTBLLABEL)} « Nom d’affichage : »  <br/> |
|Zone de modification du nom complet  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|Étiquette d’adresse de messagerie  <br/> |{0 sizeof(DTBLLABEL)} « Adresse électronique : »  <br/> |
|Zone d’édition d’adresse de messagerie  <br/> |{sizeof(DTBLEDIT), 0, 80, ADRESSE_EMAIL_PR}  <br/> |
|Case à cocher  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Les boutons **OK**, **Annuler**et **aide** ne sont pas inclus dans le tableau d’affichage. L’interface utilisateur peut ajouter le contexte à une boîte de dialogue en ajoutant des contrôles pas dans la table d’affichage. 
  
## <a name="see-also"></a>Voir aussi



[Affichage tableau implémentation](display-table-implementation.md)

