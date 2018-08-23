---
title: Utilisation des macros pour la gestion des erreurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567124"
---
# <a name="using-macros-for-error-handling"></a>Utilisation des macros pour la gestion des erreurs

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
   

