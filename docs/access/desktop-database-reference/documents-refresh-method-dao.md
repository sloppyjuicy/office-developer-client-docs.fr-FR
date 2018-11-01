---
title: Documents.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: 33405192-f23c-e2a2-feb6-9d641439cbc5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192321(v=office.15)
ms:contentKeyID: 48544100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a3070e5d07665465a5946ac8ace049576c14b04
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870183"
---
# <a name="documentsrefresh-method-dao"></a>Documents.Refresh Method (DAO)


**S’applique à**: Access 2013, Office 2013

Met à jour les objets de la collection spécifiée en fonction du schéma actuel de la base de données.

## <a name="syntax"></a>Syntaxe

*expression* . Actualiser

*expression* Variable qui représente un objet **Documents** .

## <a name="remarks"></a>Remarques

La méthode **Refresh** s'avère utile dans les environnements multi-utilisateur où d'autres utilisateurs peuvent modifier la base de données. Vous pouvez également avoir besoin de l'appliquer aux collections indirectement affectées par les modifications apportées à la base de données. Par exemple, si vous modifiez une collection **Users**, vous devrez peut-être actualiser une collection **Groups** avant d'utiliser la collection **Groups**.

Une collection est remplie d'objets lors de son premier référencement et ne reflète pas automatiquement les modifications que les autres utilisateurs apportent par la suite. S'il est probable qu'un autre utilisateur a modifié une collection, appliquez immédiatement la méthode Refresh à la collection avant d'effectuer une tâche dans votre application qui suppose la présence ou l'absence d'un objet déterminé dans la collection. Vous serez ainsi assuré que la collection est parfaitement à jour. D'un autre côté, l'utilisation de la méthode Refresh peut inutilement ralentir les performances.

