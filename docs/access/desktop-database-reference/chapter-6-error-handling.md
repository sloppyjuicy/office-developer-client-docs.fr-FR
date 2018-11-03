---
title: 'Chapitre 6 : Gestion d’erreur'
TOCTitle: 'Chapter 6: Error handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c6e4f4e4218992b89a3370375bb322adfcdd57c
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937182"
---
# <a name="chapter-6-error-handling"></a>Chapitre 6 : Gestion d’erreur

**S’applique à**: Access 2013, Office 2013

ADO utilise différentes méthodes pour avertir une application d'une erreur. Ce chapitre présente les types d'erreurs pouvant survenir lorsque vous utilisez ADO et comment votre application est avertie. Différentes façons de gérer ces erreurs sont également suggérées en fin de chapitre.

## <a name="how-does-ado-report-errors"></a>Comment ADO signale-t-il les erreurs ?

ADO vous avertit des erreurs de diverses façons :

- Les erreurs ADO génèrent une erreur d'exécution. Vous pouvez gérer une erreur ADO de la même manière que toute autre erreur d'exécution, en utilisant une instruction **Sur erreur** dans Visual Basic, par exemple.

- Votre programme peut recevoir des erreurs de la base de données OLE DB. Ce type d'erreur génère également une erreur d'exécution.

- Si l'erreur est propre à votre fournisseur de données, un ou plusieurs objets **Error** sont placés dans la collection **Errors** de l'objet **Connection** utilisé pour accéder au magasin de données au moment de l'erreur.

- Si le processus à l'origine d'un événement provoque aussi une erreur, les informations relatives à cette dernière sont placées dans un objet **Error** et transférées comme paramètre à l'événement. Reportez-vous au [Chapitre 7 : Gestion des événements ADO](chapter-7-handling-ado-events.md) pour en savoir plus sur les événements.

- Les problèmes qui surviennent pendant le traitement de mises à jour en lot ou d'autres opérations de masse impliquant un **jeu d'enregistrements** peuvent être signalés par la propriété **Status** du **jeu d'enregistrements**. Par exemple, les violations de restrictions de schémas ou des autorisations insuffisantes peuvent être spécifiées par des valeurs **RecordStatusEnum**.

- Les problèmes impliquant un **champ** particulier dans l'enregistrement actif sont également signalés par la propriété **Status** de chaque **champ** de la collection **Fields** de l' **enregistrement** ou du **jeu d'enregistrements**. Par exemple, les mises à jour interrompues ou les types de données incompatibles peuvent être spécifiés par les valeurs **FieldStatusEnum**.

Les sections ci-après décrivent plus en détail chacune de ces méthodes de notification.

- [Erreurs ADO](ado-errors.md)
- [Référence des erreurs ADO](ado-error-reference.md)
- [Erreurs du fournisseur](provider-errors.md)
- [Informations sur les erreurs relatives aux champs](field-related-error-information.md)
- [Informations d’erreurs liées au jeu d’enregistrements](recordset-related-error-information.md)
- [Anticipation des erreurs](anticipating-errors.md)
- [Gestion des erreurs dans d’autres langues (ADO)](handling-errors-in-other-languages.md)