---
title: PROPRIÉTÉ URL (RDS - Référence de base de données de bureau Access)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c05bf1051a6c84d40225af8799c9ab2a4486331e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576827"
---
# <a name="url-property-rds"></a>PROPRIÉTÉ URL (RDS)

**S’applique à** : Access 2013, Office 2013

Indique une chaîne contenant une URL relative ou absolue.

Vous pouvez définir la propriété **URL** au moment de la création dans la balise OBJECT de l'objet [DataControl](datacontrol-object-rds.md) ou en mode exécution dans le code de script.

## <a name="syntax"></a>Syntaxe

Moment de la conception : \<PARAM NAME="URL" VALUE="Server"\>

Durée d’application : DataControl.URL="Server »

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Serveur* |Valeur **String** contenant une URL valide.|
|*DataControl* |Variable d'objet représentant un objet **DataControl**.|

## <a name="remarks"></a>Remarques

L'URL identifie généralement un fichier ASP (.asp) qui peut produire et renvoyer un [Recordset](recordset-object-ado.md). L'utilisateur peut ainsi obtenir un **Recordset** sans avoir à appeler l'objet serveur [DataFactory](datafactory-object-rdsserver.md) ou programmer un objet métier personnalisé.

Si la propriété **URL** a été définie, [SubmitChanges](submitchanges-method-rds.md) soumettra des modifications à l'emplacement spécifié par l'URL.

