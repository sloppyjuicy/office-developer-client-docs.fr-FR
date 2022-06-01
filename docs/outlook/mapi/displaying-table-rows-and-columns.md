---
title: Affichage des lignes et des colonnes de tableau
description: Décrit comment afficher des lignes et des colonnes de tableau, qui peuvent être utilisées par un fournisseur de carnet d’adresses pour permettre aux utilisateurs de définir de nouveaux destinataires de courrier.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
ms.openlocfilehash: 3c253afad2c39638eaf02542a15228ae571d9fae
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816688"
---
# <a name="displaying-table-rows-and-columns"></a>Affichage des lignes et des colonnes de tableau

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Une page de propriétés peut être utilisée par un fournisseur de carnet d’adresses pour permettre aux utilisateurs de définir de nouveaux destinataires de courrier. 
  
La table d’affichage correspondante contient quatre lignes, une pour chaque contrôle. Les valeurs des colonnes qui indiquent la position sont les suivantes.
  
|**Contrôle**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|Étiquette de nom d’affichage  <br/> |14  <br/> |18   <br/> |49  <br/> |8   <br/> |
|Zone d’édition du nom d’affichage  <br/> |76  <br/> |16  <br/> |89  <br/> |12   <br/> |
|Étiquette d’adresse e-mail  <br/> |14  <br/> |42  <br/> |50  <br/> |8   <br/> |
|Zone d’édition de l’adresse e-mail  <br/> |76  <br/> |40  <br/> |89  <br/> |12   <br/> |
|Case à cocher  <br/> |14  <br/> |64  <br/> |90  <br/> |12   <br/> |
   
Ce tableau suivant suggère des valeurs appropriées pour le type du contrôle, sa propriété **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) et le masque de bits des indicateurs, sa propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
  
|**Contrôle**|**Type (Type)**|**Flags**|
|:-----|:-----|:-----|
|Étiquette de nom d’affichage  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Zone d’édition du nom d’affichage  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE \| DT_REQUIRED  <br/> |
|Étiquette d’adresse e-mail  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Zone d’édition de l’adresse e-mail  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE \| DT_REQUIRED  <br/> |
|Case à cocher  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
Le tableau final répertorie chaque contrôle avec le contenu de sa structure de contrôle associée. Notez que la valeur de chacun des contrôles d’étiquette s’affiche en mémoire directement après la structure.
  
|**Contrôle**|**Structure**|
|:-----|:-----|
|Étiquette de nom d’affichage  <br/> |{sizeof(DTBLLABEL), 0} « Nom d’affichage: »  <br/> |
|Zone d’édition du nom d’affichage  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|Étiquette d’adresse e-mail  <br/> |{sizeof(DTBLLABEL), 0} « Adresse e-mail : »  <br/> |
|Zone d’édition de l’adresse e-mail  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Case à cocher  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Les boutons **OK**, **Annuler** et **Aide** ne sont pas inclus dans la table d’affichage. L’interface utilisateur peut ajouter du contexte à une boîte de dialogue en ajoutant des contrôles qui ne sont pas dans la table d’affichage. 
  
## <a name="see-also"></a>Voir aussi



[Implémentation de table d’affichage](display-table-implementation.md)

