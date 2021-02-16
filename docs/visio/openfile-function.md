---
title: OPENFILE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Ouvre un document Microsoft Visio, s’il n’est pas déjà ouvert, et active la fenêtre de document.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419575"
---
# <a name="openfile-function"></a>Fonction OPENFILE

Ouvre un document Microsoft Visio, s’il n’est pas déjà ouvert, et active la fenêtre de document.
  
## <a name="syntax"></a>Syntaxe

 **OPENFILE**( _« filename »_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |Obligatoire  <br/> |**String** <br/> |Nom du fichier, y compris le chemin d’accès au fichier, que vous souhaitez ouvrir.  <br/> |
   
## <a name="remarks"></a>Remarques

Si plusieurs fonctions OPENFILE sont déclenchées, elles sont mises en file d’attente et exécutées dans l’ordre d’évaluation. Si le document Visio ouvert est activé pour une modification à l’écran (dans une autre application), une nouvelle copie de Visio est lancée avec le nom de fichier demandé. 
  
Cette fonction renvoie toujours la valeur FALSE. 
  
Dans les versions précédentes de Visio, cette fonction s’appelait _OPENFILE. Les versions Visio 4.0 et ultérieures acceptent les deux styles. 
  
## <a name="example"></a>Exemple

 `OPENFILE("C:/MyFile.vsdx")`
  
Ouvre le fichier spécifié « MyFile.vsdx » dans une nouvelle fenêtre ou active la fenêtre si le fichier est déjà ouvert. 
  

