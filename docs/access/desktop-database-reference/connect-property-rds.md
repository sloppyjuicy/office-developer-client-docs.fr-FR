---
title: Connect, propriété (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ebd9eb25e2e0e6b9b2233ff0d9faf8c3e369f0f9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925260"
---
# <a name="connect-property-rds"></a>Connect, propriété (RDS)


**S’applique à**: Access 2013, Office 2013

Indique le nom de la base de données dans laquelle les opérations de requête et de mise à jour sont exécutées.

Vous pouvez définir la propriété **Connect** au moment du design dans les balises OBJECT de l'objet [RDS.DataControl](datacontrol-object-rds.md) ou au moment de l'exécution dans le code de script (par exemple, VBScript).

## <a name="syntax"></a>Syntaxe

Au moment du design : \<PARAM NAME = « Connexion », valeur = « ConnectionString »\>

Temps d’exécution : DataControl.Connect = « ConnectionString »

## <a name="parameters"></a>Paramètres

- *ConnectionString*

  - Chaîne de connexion valide. Pour plus d'informations d'ordre général sur les chaînes de connexion, reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md) ou à la documentation du fournisseur.
    
    > [!NOTE]
    > [!REMARQUE] Si vous spécifiez MS Remote comme fournisseur de l'objet **RDS.DataControl**, un scénario à quatre niveaux est créé. Les scénarios comptant plus de trois niveaux n'ont pas été testés et sont normalement inutiles.

- *DataControl*

  - Une variable objet qui représente un objet **RDS.DataControl**.

