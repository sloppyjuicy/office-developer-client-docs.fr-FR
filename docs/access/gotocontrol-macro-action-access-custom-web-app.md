---
title: Action de macro AtteindreContrôle (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Vous pouvez utiliser l’action AtteindreContrôle pour déplacer le focus sur le contrôle spécifié dans l’enregistrement actif de la vue ouverte.
ms.openlocfilehash: 5323f1daff2e8ae76c9aa24e6a40b907b6396030
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572472"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a>Action de macro AtteindreContrôle (application web personnalisée Access)

Vous pouvez utiliser l’action **AtteindreContrôle** pour déplacer le focus sur le contrôle spécifié dans l’enregistrement actif de la vue ouverte. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

L’action **AtteindreContrôle** possède l’argument suivant. 
  
|**Argument de l’action**|**Description**|
|:-----|:-----|
|**Nom du contrôle** : <br/> |Nom du champ ou du contrôle dans lequel vous souhaitez déplacer le focus. Cet argument est obligatoire.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette action lorsque vous souhaitez mettre le focus sur un champ ou un contrôle particulier. Vous pouvez également utiliser cette action pour naviguer dans un formulaire sous certaines conditions. Par exemple, si l'utilisateur saisit non dans un contrôle conjoint sur un formulaire d'assurance maladie, le focus peut automatiquement passer le contrôle nom du conjoint/partenaire et déplacer vers le contrôle suivant.
  

