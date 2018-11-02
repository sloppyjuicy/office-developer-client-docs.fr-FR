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
ms.openlocfilehash: 1723deea7f29c59fb388a11acc5e5ffcced4abe1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924595"
---
# <a name="dbengineversion-property-dao"></a>Propriété DBEngine.Version (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie la version de DAO en cours d'utilisation. Valeur de type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Version

*expression* Variable qui représente un objet **DBEngine** .

## <a name="remarks"></a>Remarques

La valeur renvoyée est une chaîne (type String) correspondant à un numéro de version au format « principale.secondaire ». Par exemple, « 3.0 ». Le numéro de version du produit comprend le numéro de version principale (3), un point, puis le numéro de version secondaire (0).

