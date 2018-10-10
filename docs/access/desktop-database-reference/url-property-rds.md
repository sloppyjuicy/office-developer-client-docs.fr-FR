---
title: URL, propriété (RDS - référence du bureau de la base de données Access)
TOCTitle: URL Property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8d1e524df8f1921f712f9dce174ab90ebd57325
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469060"
---
# <a name="url-property-rds"></a>URL, propriété (RDS)


**S’applique à**: Access 2013 | Office 2013



Indique une chaîne contenant une URL relative ou absolue.

Vous pouvez définir la propriété **URL** au moment de la création dans la balise OBJECT de l'objet [DataControl](datacontrol-object-rds.md) ou en mode exécution dans le code de script.

## <a name="syntax"></a>Syntaxe

Au moment du design : \<PARAM NAME = valeur « URL » = « Serveur »\>

Temps d’exécution : DataControl.URL="Server »

## <a name="parameters"></a>Paramètres

  - *Serveur*

  - Valeur **String** contenant une URL valide.

  - *DataControl*

  - Variable d'objet représentant un objet **DataControl**.

## <a name="remarks"></a>Remarques

L'URL identifie généralement un fichier ASP (.asp) qui peut produire et renvoyer un [Recordset ](recordset-object-ado.md). L'utilisateur peut ainsi obtenir un **Recordset** sans avoir à appeler l'objet serveur [DataFactory](datafactory-object-rdsserver.md) ou programmer un objet métier personnalisé.

Si la propriété **URL** a été définie, [SubmitChanges](submitchanges-method-rds.md) soumettra des modifications à l'emplacement spécifié par l'URL.

