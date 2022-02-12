---
title: UNICHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
ms.localizationpriority: medium
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Renvoie le caractère Unicode d’un nombre.
ms.openlocfilehash: 75d907e4aa06ab531c28aad031b8e76682a1ea19
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771058"
---
# <a name="unichar-function"></a>Fonction UNICHAR

Renvoie le caractère Unicode d’un nombre. 
  
## <a name="syntax"></a>Syntaxe

UNICHAR (** *nombre* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Entier compris entre 1 et 65 535 (inclus), ou la fonction renvoie une erreur. |
   
## <a name="remarks"></a>Remarques

La chaîne obtenue présente une longueur d’un caractère unicode (deux caractères). 
  
## <a name="example"></a>Exemple

UNICHAR(65) 
  
Renvoie A (lettre majuscule latine A) 
  

