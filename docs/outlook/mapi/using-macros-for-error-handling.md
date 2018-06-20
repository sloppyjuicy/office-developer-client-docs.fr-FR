---
title: Utilisation de Macros pour la gestion des erreurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c4e216f2204f4ee97d9eeac81f77ce6a82fff3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787445"
---
# <a name="using-macros-for-error-handling"></a>Utilisation de Macros pour la gestion des erreurs

  
  
**S’applique à**: Outlook 
  
Il existe plusieurs macros pour rendre plus facile d’utiliser des valeurs HRESULT.
  
Il existe deux jeux de macros de l’échec ou la réussite de test : HR_SUCCEEDED et HR_FAILED et a réussi et a échoué. A réussi est qu'identique à HR_SUCCEEDED et l’échec est identique à HR_FAILED.
  
Dans ce cas, utilisez la macro **ResultFromScode** pour définir la variable HRESULT à la valeur HRESULT de S_OK. 
  
Macros couramment utilisés sont décrites brièvement dans le tableau suivant.
  
|**Macro**|**Description**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Construit une valeur HRESULT de ses composants.  <br/> |
|**HR_SUCCEEDED** <br/> |Teste une valeur HRESULT pour un succès ou un avertissement.  <br/> |
|**HR_FAILED** <br/> |Teste une valeur HRESULT pour une condition d’erreur.  <br/> |
|**HRESULT_CODE** <br/> |Extrait la partie de code d’erreur de HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrait la facilité de HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrait le bit gravité la gravité.  <br/> |
|**A RÉUSSI** <br/> |Teste une valeur HRESULT pour un succès ou un avertissement.  <br/> |
|**A ÉCHOUÉ** <br/> |Teste une valeur HRESULT pour une condition d’erreur.  <br/> |
   

