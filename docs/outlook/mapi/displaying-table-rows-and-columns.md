---
title: Affichage des lignes et des colonnes d'un tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f9f1cc0bebf3c90a5c12f2714e8ab7eea59104da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337022"
---
# <a name="displaying-table-rows-and-columns"></a>Affichage des lignes et des colonnes d'un tableau

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Une page de propriétés peut être utilisée par un fournisseur de carnets d'adresses pour permettre aux utilisateurs de définir de nouveaux destinataires de courrier électronique. 
  
Le tableau d'affichage correspondant contient quatre lignes, une pour chaque contrôle. Les valeurs des colonnes qui indiquent la position sont les suivantes.
  
|**Contrôle**|**XPOS**|**YPOS**|**DELTAX**|**DELTAy**|
|:-----|:-----|:-----|:-----|:-----|
|Étiquette de nom d'affichage  <br/> |13  <br/> |18  <br/> |49  <br/> |8bits  <br/> |
|Zone d'édition nom complet  <br/> |76  <br/> |Seiz  <br/> |89  <br/> |an  <br/> |
|Étiquette d'adresse de messagerie  <br/> |13  <br/> |42  <br/> |50  <br/> |8bits  <br/> |
|Zone d'édition adresse de messagerie  <br/> |76  <br/> |40  <br/> |89  <br/> |an  <br/> |
|Case à cocher  <br/> |13  <br/> |64  <br/> |90  <br/> |an  <br/> |
   
Le tableau suivant indique les valeurs appropriées pour le type du contrôle, sa propriété **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) et son masque de réindicateur, sa propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
  
|**Contrôle**|**Type**|**Flags**|
|:-----|:-----|:-----|
|Étiquette de nom d'affichage  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Zone d'édition nom complet  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Étiquette d'adresse de messagerie  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Zone d'édition adresse de messagerie  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Case à cocher  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
Le tableau final répertorie chaque contrôle avec le contenu de sa structure de contrôle associée. Notez que la valeur de chacun des contrôles Label apparaît en mémoire directement après la structure.
  
|**Contrôle**|**Structure**|
|:-----|:-----|
|Étiquette de nom d'affichage  <br/> |{sizeof (DTBLLABEL), 0} «Nom complet:»  <br/> |
|Zone d'édition nom complet  <br/> |{sizeof (DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|Étiquette d'adresse de messagerie  <br/> |{sizeof (DTBLLABEL), 0} «Adresse de messagerie:»  <br/> |
|Zone d'édition adresse de messagerie  <br/> |{sizeof (DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Case à cocher  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Les boutons **OK**, **Annuler**et **aide** ne sont pas inclus dans la table d'affichage. L'interface utilisateur peut ajouter un contexte à une boîte de dialogue en ajoutant des contrôles qui ne sont pas dans la table d'affichage. 
  
## <a name="see-also"></a>Voir aussi



[Implémentation des tables d'affichage](display-table-implementation.md)

