---
title: Charset, propriété (ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ca38e10402a8353d6a32a8cd288bd72ce4ec60e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562831"
---
# <a name="charset-property-ado"></a>Charset, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le jeu de caractères dans lequel le contenu d'un objet [Stream](stream-object-ado.md) de type texte doit être converti pour être stocké dans la mémoire tampon interne des objets Stream.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String** qui spécifie le jeu de caractères dans lequel le contenu de l'objet **Stream** est converti. La valeur par défaut est « Unicode ». Les valeurs admises sont des chaînes classiques transmises via l'interface sous forme de chaînes de jeu de caractères Internet (par exemple, « ISO-8859-1 », « Windows-1252 », etc.). Pour obtenir la liste des chaînes de jeu de caractères connues par un système, voir les sous-clés de hKEY \_ CLASSES \_ ROOT \\ MIME \\ Database Charset dans le Registre \\ Windows.

## <a name="remarks"></a>Remarques

Dans un objet **Stream** de type texte, les données de texte sont stockées dans le jeu de caractères spécifié par la propriété **Charset**. La valeur par défaut est Unicode. La propriété **Charset** est utilisée pour convertir des données accédant à l'objet **Stream** ou provenant de l'objet **Stream**. Par exemple, si l'objet **Stream** contient des données au format ISO-8859-1 et que ces données sont copiées dans un BSTR, l'objet **Stream** convertit les données au format Unicode. L'inverse est vrai également.

Pour un objet **Stream** ouvert, la propriété [Position](position-property-ado.md) actuelle doit se trouver au début de l'objet **Stream** (0) pour pouvoir définir la propriété **Charset**.

La propriété **Charset** n’est utilisée qu’avec des objets **Stream** de type texte ([Type](type-property-ado-stream.md) a la valeur **adTypeText**). Cette propriété est ignorée si **Type** a la valeur **adTypeBinary**.

