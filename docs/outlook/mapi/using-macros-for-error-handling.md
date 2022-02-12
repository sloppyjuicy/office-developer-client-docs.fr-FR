---
title: Utilisation de macros pour la gestion des erreurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f3d464effa1ba4c906acf7bd83645ad51938852e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773046"
---
# <a name="using-macros-for-error-handling"></a>Utilisation de macros pour la gestion des erreurs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe plusieurs macros qui facilitent l’emploi des valeurs HRESULT.
  
Il existe deux ensembles de macros qui testent l’échec ou la réussite : HR_SUCCEEDED et HR_FAILED et SUCCEEDED et FAILED. SUCCEEDED est identique à HR_SUCCEEDED et FAILED est identique à HR_FAILED.
  
Dans ce cas, utilisez la macro **ResultFromScode** pour définir la variable HRESULT sur la valeur HRESULT correspondante pour S_OK. 
  
Les macros couramment utilisées sont brièvement décrites dans le tableau suivant.
  
|**Macro**|**Description**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Construit un HRESULT à partir de ses composants. |
|**HR_SUCCEEDED** <br/> |Teste un HRESULT pour une condition de réussite ou d’avertissement. |
|**HR_FAILED** <br/> |Teste une condition d’erreur HRESULT. |
|**HRESULT_CODE** <br/> |Extrait la partie code d’erreur du HRESULT. |
|**HRESULT_FACILITY** <br/> |Extrait la fonction du HRESULT. |
|**HRESULT_SEVERITY** <br/> |Extrait le bit de gravité de la GRAVITÉ. |
|**SUCCEEDED** <br/> |Teste un HRESULT pour une condition de réussite ou d’avertissement. |
|**FAILED** <br/> |Teste une condition d’erreur HRESULT. |
   

