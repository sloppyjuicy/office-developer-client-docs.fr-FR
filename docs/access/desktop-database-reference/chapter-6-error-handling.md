---
title: 'Chapitre 6 : Gestion des erreurs'
TOCTitle: 'Chapter 6: Error Handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e00f762ac76023f3f720d8e7341c517b932e3f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469440"
---
# <a name="chapter-6-error-handling"></a>Chapitre 6 : Gestion des erreurs


**S’applique à**: Access 2013 | Office 2013

ADO utilise différentes méthodes pour avertir une application d'une erreur. Ce chapitre présente les types d'erreurs pouvant survenir lorsque vous utilisez ADO et comment votre application est avertie. Différentes façons de gérer ces erreurs sont également suggérées en fin de chapitre.

## <a name="how-does-ado-report-errors"></a>Comment ADO signale-t-il les erreurs ?

ADO vous avertit des erreurs de diverses façons :

  - Les erreurs ADO génèrent une erreur d'exécution. Vous pouvez gérer une erreur ADO de la même manière que toute autre erreur d'exécution, en utilisant une instruction **Sur erreur** dans Visual Basic, par exemple.

  - Votre programme peut recevoir des erreurs de la base de données OLE DB. Ce type d'erreur génère également une erreur d'exécution.

  - Si l'erreur est propre à votre fournisseur de données, un ou plusieurs objets **Error** sont placés dans la collection **Errors** de l'objet **Connection** utilisé pour accéder au magasin de données au moment de l'erreur.

  - Si le processus à l'origine d'un événement provoque aussi une erreur, les informations relatives à cette dernière sont placées dans un objet **Error** et transférées comme paramètre à l'événement. Reportez-vous au [Chapitre 7 : Gestion des événements ADO](chapter-7-handling-ado-events.md) pour en savoir plus sur les événements.

  - Les problèmes qui surviennent pendant le traitement de mises à jour en lot ou d'autres opérations de masse impliquant un **jeu d'enregistrements** peuvent être signalés par la propriété **Status** du **jeu d'enregistrements**. Par exemple, les violations de restrictions de schémas ou des autorisations insuffisantes peuvent être spécifiées par des valeurs **RecordStatusEnum**.

  - Les problèmes impliquant un **champ** particulier dans l'enregistrement actif sont également signalés par la propriété **Status** de chaque **champ** de la collection **Fields** de l' **enregistrement** ou du **jeu d'enregistrements**. Par exemple, les mises à jour interrompues ou les types de données incompatibles peuvent être spécifiés par les valeurs **FieldStatusEnum**.

Les sections ci-après décrivent plus en détail chacune de ces méthodes de notification.

