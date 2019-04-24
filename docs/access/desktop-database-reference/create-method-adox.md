---
title: Create, méthode (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295421"
---
# <a name="create-method-adox"></a>Create, méthode (ADOX)

**S’applique à** : Access 2013, Office 2013

Crée un catalogue.

## <a name="syntax"></a>Syntaxe

*Catalogue*. Créer*connectString*

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*ConnectString* |Valeur de type **String** utilisée pour se connecter à la source de données.|

## <a name="remarks"></a>Remarques

La méthode **Create** crée et ouvre un nouvel objet ADO [Connection](connection-object-ado.md) à la source de données spécifiée dans le paramètre *ConnectString*. En cas de réussite, le nouvel objet **Connection** est affecté à la propriété [ActiveConnection](activeconnection-property-adox.md).

Une erreur se produit si le fournisseur ne prend pas en charge la création de catalogues.

