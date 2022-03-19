---
title: Affichage des lignes et des colonnes du tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2fbedd849824324bbad2e6106007c8151f824f66
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627150"
---
# <a name="displaying-table-rows-and-columns"></a>Affichage des lignes et des colonnes du tableau

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Une page de propriétés peut être utilisée par un fournisseur de carnet d’adresses pour permettre aux utilisateurs de définir de nouveaux destinataires de messagerie. 
  
Le tableau d’affichage correspondant contient quatre lignes, une pour chaque contrôle. Les valeurs des colonnes qui indiquent la position sont les suivantes.
  
|**Contrôle**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|Étiquette de nom d’affichage  <br/> |14   <br/> |18   <br/> |49  <br/> |8   <br/> |
|Zone d’édition du nom d’affichage  <br/> |76  <br/> |16  <br/> |89  <br/> |12   <br/> |
|Étiquette d’adresse de messagerie  <br/> |14   <br/> |42  <br/> |50  <br/> |8   <br/> |
|Zone de modification d’adresse de messagerie  <br/> |76  <br/> |40  <br/> |89  <br/> |12   <br/> |
|Case à cocher  <br/> |14   <br/> |64  <br/> |90  <br/> |12   <br/> |
   
Le tableau suivant suggère les valeurs appropriées pour le type du contrôle, sa propriété **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) et le masque de bits d’indicateurs, sa propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
  
|**Contrôle**|**Type**|**Flags**|
|:-----|:-----|:-----|
|Étiquette de nom d’affichage  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Zone d’édition du nom d’affichage  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE \| DT_REQUIRED  <br/> |
|Étiquette d’adresse de messagerie  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Zone de modification d’adresse de messagerie  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE \| DT_REQUIRED  <br/> |
|Case à cocher  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
Le tableau final répertorie chaque contrôle avec le contenu de sa structure de contrôle associée. Notez que la valeur de chacun des contrôles d’étiquette s’affiche en mémoire directement après la structure.
  
|**Contrôle**|**Structure**|
|:-----|:-----|
|Étiquette de nom d’affichage  <br/> |{sizeof(DTBLLABEL), 0} « Nom complet : »  <br/> |
|Zone d’édition du nom d’affichage  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|Étiquette d’adresse de messagerie  <br/> |{sizeof(DTBLLABEL), 0} « Adresse e-mail : »  <br/> |
|Zone de modification d’adresse de messagerie  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Case à cocher  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Les **boutons OK**, **Annuler** et **Aide** ne sont pas inclus dans le tableau d’affichage. L’interface utilisateur peut ajouter du contexte à une boîte de dialogue en ajoutant des contrôles qui ne sont pas dans le tableau d’affichage. 
  
## <a name="see-also"></a>Consultez aussi



[Implémentation du tableau d’affichage](display-table-implementation.md)

