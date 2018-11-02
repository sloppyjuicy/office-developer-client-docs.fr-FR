---
title: Méthode Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c97786db2e909074f1a1e0d81e4af03d34301602
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920682"
---
# <a name="databaseclose-method-dao"></a>Méthode Database.Close (DAO)


**S’applique à**: Access 2013, Office 2013

Ferme un objet **Database** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* . Fermer

*expression* Variable qui représente un objet de **base de données** .

## <a name="remarks"></a>Remarques

Si l'objet **Database** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.

Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).

