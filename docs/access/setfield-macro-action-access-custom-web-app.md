---
title: SetField, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: L'action DéfinirChamp peut être utilisée pour assigner une valeur à un champ.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432925"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>SetField, action de macro (application Web personnalisée Access)

L'action **DéfinirChamp** peut être utilisée pour assigner une valeur à un champ. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> L’action **DéfinirChamp** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Setting

L’action **DéfinirChamp** utilise les arguments répertoriés dans le tableau suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
|**Nom** <br/> |Chaîne qui identifie le champ.  <br/> |
|**Valeur** <br/> |Expression qui spécifie la valeur à assigner au champ.  <br/> |
   
## <a name="remarks"></a>Remarques

L'action **SetField** ne peut pas être utilisée en dehors d'un bloc de données **[CréerEnregistrement](createrecord-data-block-access-custom-web-app.md)** ou **[EditRecord](editrecord-data-block-access-custom-web-app.md)** . 
  

