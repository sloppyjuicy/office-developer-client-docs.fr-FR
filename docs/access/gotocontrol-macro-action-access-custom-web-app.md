---
title: Action de macro AtteindreContrôle (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Vous pouvez utiliser l’action AtteindreContrôle pour déplacer le focus sur le contrôle spécifié dans l’enregistrement actif de la vue ouverte.
ms.openlocfilehash: cdb73bec6adea2841fddb1fcab450d1ac41c32b6
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62789367"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a>Action de macro AtteindreContrôle (application web personnalisée Access)

Vous pouvez utiliser l’action **AtteindreContrôle** pour déplacer le focus sur le contrôle spécifié dans l’enregistrement actif de la vue ouverte. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

L’action **AtteindreContrôle** possède l’argument suivant. 
  
|**Argument de l’action**|**Description**|
|:-----|:-----|
|**Nom du contrôle** : <br/> |Nom du champ ou du contrôle dans lequel vous souhaitez déplacer le focus. Cet argument est obligatoire. |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette action lorsque vous souhaitez mettre le focus sur un champ ou un contrôle particulier. Vous pouvez également utiliser cette action pour naviguer dans un formulaire sous certaines conditions. Par exemple, si l'utilisateur saisit non dans un contrôle conjoint sur un formulaire d'assurance maladie, le focus peut automatiquement passer le contrôle nom du conjoint/partenaire et déplacer vers le contrôle suivant.
  

