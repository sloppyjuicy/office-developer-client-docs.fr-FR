---
title: Anticipation des erreurs
TOCTitle: Anticipating errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 044f5ab8a76b6736ac45bc332d155f5ad5d801ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559058"
---
# <a name="anticipating-errors"></a>Anticipation des erreurs


**S’applique à** : Access 2013, Office 2013

La prévention des erreurs est tout aussi importante que leur gestion. Cette dernière section contient une courte liste des précautions à prendre dans votre application pour réduire le nombre d'erreurs éventuelles.

Vérifiez l'état des objets en contrôlant la valeur de la propriété **State** avant d'exécuter une opération avec ces objets. Par exemple, si votre application utilise un objet **Connection** global, vérifiez sa propriété **State** pour savoir s'il est déjà ouvert avant d'appeler la méthode **Open**.

- Tout programme qui accepte des données d'un utilisateur doit inclure du code visant à valider les données avant de les envoyer au magasin de données. Vous ne pouvez pas compter sur le magasin de données, le fournisseur, ADO ou même votre langage de programmation pour signaler des problèmes. Vous devez vérifier chaque octet entré par vos utilisateurs et vous assurer que les données des champs sont correctes et que les champs obligatoires ne sont pas vides.

Vérifiez les données avant d'essayer de les inscrire dans un magasin de données. Pour ce faire, la méthode la plus simple consiste à gérer les événements **WillMove** ou **WillUpdateRecordset**. Pour une explication plus complète de la gestion des événements ADO, consultez le [chapitre 7 : Gestion des événements ADO](chapter-7-handling-ado-events.md).

Assurez-vous que les objets **Record** ne sont pas en dehors des limites de l'objet **Recordset** avant de déplacer le pointeur d'enregistrements. Si vous essayez d'exécuter la méthode **MoveNext** lorsque la propriété **EOF** a la valeur True ou **MovePrev** lorsque la propriété **BOF** a la valeur True, une erreur se produit. Si vous exécutez les méthodes **Move** lorsque les propriétés **EOF** et **BOF** ont la valeur True, une erreur est générée.

Des erreurs se produisent si vous essayez d'effectuer des opérations, telles que **Seek** et **Find** sur un objet **Recordset** vide.

