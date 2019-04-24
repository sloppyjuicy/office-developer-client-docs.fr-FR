---
title: Utilisation de macros pour la gestion des erreurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329657"
---
# <a name="using-macros-for-error-handling"></a>Utilisation de macros pour la gestion des erreurs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe plusieurs macros permettant de faciliter l'utilisation des valeurs HRESULT.
  
Il existe deux jeux de macros qui testent les échecs ou les réussites: HR_SUCCEEDED et HR_FAILED et FAILed et FAILed. SUCCEEDED est identique à HR_SUCCEEDED et FAILed est identique à HR_FAILED.
  
Dans ce cas, utilisez la macro **ResultFromScode** pour définir la variable HRESULT sur la valeur HRESULT correspondante pour S_OK. 
  
Les macros couramment utilisées sont brièvement décrites dans le tableau suivant.
  
|**Macro**|**Description**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Construit un HRESULT à partir de ses composants.  <br/> |
|**HR_SUCCEEDED** <br/> |Teste un HRESULT pour une condition de réussite ou d'avertissement.  <br/> |
|**HR_FAILED** <br/> |Teste un HRESULT pour une condition d'erreur.  <br/> |
|**HRESULT_CODE** <br/> |Extrait la partie de code d'erreur du HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrait l'installation du HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrait le bit de gravité de la gravité.  <br/> |
|**TERMINÉ** <br/> |Teste un HRESULT pour une condition de réussite ou d'avertissement.  <br/> |
|**Echec** <br/> |Teste un HRESULT pour une condition d'erreur.  <br/> |
   

