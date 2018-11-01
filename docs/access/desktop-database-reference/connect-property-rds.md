---
title: Connect, propriété (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d9b901f925ccc009a12ef527f7bc857515042c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872402"
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

