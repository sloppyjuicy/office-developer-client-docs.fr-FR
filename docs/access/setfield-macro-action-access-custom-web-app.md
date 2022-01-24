---
title: SetField Macro Action (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: L'action DéfinirChamp peut être utilisée pour assigner une valeur à un champ.
ms.openlocfilehash: 21b765b238f7bdb5c7507ae84a813891d676e0cb
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180368"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>SetField Macro Action (Access custom web app)

L'action **DéfinirChamp** peut être utilisée pour assigner une valeur à un champ. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> L’action **DéfinirChamp** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Setting

L’action **DéfinirChamp** utilise les arguments répertoriés dans le tableau suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
|**Nom** <br/> |Chaîne qui identifie le champ.  <br/> |
|**Valeur** <br/> |Expression qui spécifie la valeur à affecter au champ.  <br/> |
   
## <a name="remarks"></a>Remarques

**L’action DéfinirField** ne peut pas être utilisée en dehors d’un bloc de données **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** ou **[EditRecord.](editrecord-data-block-access-custom-web-app.md)** 
  

