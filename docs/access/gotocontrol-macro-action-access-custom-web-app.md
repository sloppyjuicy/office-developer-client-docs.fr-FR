---
title: Action de macro AtteindreContrôle (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Vous pouvez utiliser l’action AtteindreContrôle pour déplacer le focus sur le contrôle spécifié dans l’enregistrement actif de la vue ouverte.
ms.openlocfilehash: 2368933a6277615554a565d3bdd973f7d1f366f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436474"
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
  

