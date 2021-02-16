---
title: UNICHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Renvoie le caractère Unicode d’un nombre.
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417580"
---
# <a name="unichar-function"></a>Fonction UNICHAR

Renvoie le caractère Unicode d’un nombre. 
  
## <a name="syntax"></a>Syntaxe

UNICHAR (** *nombre* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Entier compris entre 1 et 65 535 (inclus), ou la fonction renvoie une erreur.  <br/> |
   
## <a name="remarks"></a>Remarques

La chaîne obtenue présente une longueur d’un caractère unicode (deux caractères). 
  
## <a name="example"></a>Exemple

UNICHAR(65) 
  
Renvoie A (lettre majuscule latine A) 
  

