---
title: Utilisation de macros pour la gestion des erreurs
description: Décrit plusieurs macros pour faciliter l’utilisation des valeurs HRESULT dans Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
ms.openlocfilehash: 0c53ffbbf1c8ca69b3c87065fe04504f67f2722b
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894480"
---
# <a name="using-macros-for-error-handling"></a>Utilisation de macros pour la gestion des erreurs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe plusieurs macros pour faciliter l’utilisation des valeurs HRESULT.
  
Il existe deux ensembles de macros qui testent l’échec ou la réussite : HR_SUCCEEDED et HR_FAILED et SUCCEEDED et FAILED. SUCCEEDED est identique à HR_SUCCEEDED et FAILED est identique à HR_FAILED.
  
Dans ce cas, utilisez la macro **ResultFromScode** pour définir la variable HRESULT sur la valeur HRESULT correspondante pour S_OK. 
  
Les macros couramment utilisées sont brièvement décrites dans le tableau suivant.
  
|**Macro**|**Description**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Construit un HRESULT à partir de ses composants. |
|**HR_SUCCEEDED** <br/> |Teste un HRESULT pour une condition de réussite ou d’avertissement. |
|**HR_FAILED** <br/> |Teste un HRESULT pour une condition d’erreur. |
|**HRESULT_CODE** <br/> |Extrait la partie code d’erreur du HRESULT. |
|**HRESULT_FACILITY** <br/> |Extrait l’installation du HRESULT. |
|**HRESULT_SEVERITY** <br/> |Extrait le bit de gravité de la gravité. |
|**RÉUSSI** <br/> |Teste un HRESULT pour une condition de réussite ou d’avertissement. |
|**ÉCHOUÉ** <br/> |Teste un HRESULT pour une condition d’erreur. |
   

