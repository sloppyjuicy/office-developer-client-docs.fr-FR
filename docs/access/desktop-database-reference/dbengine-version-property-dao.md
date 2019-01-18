---
title: Propriété DBEngine.Version (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7e22645127f18ad815c398fd38f9ac4615dfadc9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712784"
---
# <a name="dbengineversion-property-dao"></a>Propriété DBEngine.Version (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie la version de DAO en cours d'utilisation. Valeur de type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Version

*expression* Variable qui représente un objet **DBEngine** .

## <a name="remarks"></a>Remarques

La valeur renvoyée est une chaîne (type String) correspondant à un numéro de version au format « principale.secondaire ». Par exemple, « 3.0 ». Le numéro de version du produit comprend le numéro de version principale (3), un point, puis le numéro de version secondaire (0).

