---
title: 'Chapitre 12 : Didacticiel RDS'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 276e8989b674c61414c42428bbff795bf700c6dc
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947678"
---
# <a name="chapter-12-rds-tutorial"></a>Chapitre 12 : Didacticiel RDS

**S’applique à**: Access 2013, Office 2013

Ce didacticiel illustre l'utilisation du modèle de programmation RDS pour interroger et mettre à jour une source de données. Dans un premier temps, il décrit les étapes à suivre pour accomplir cette tâche. Ensuite, le didacticiel est répété dans Microsoft Visual Basic Scripting Edition et Microsoft Visual J ++, visionnez ADO pour Windows Foundation Classes (ADO/WFC).

Ce didacticiel est codé dans différents langages pour deux raisons :

- La documentation portant sur RDS part du principe que le lecteur code en Visual Basic. Si cette documentation s'avère utile pour les programmeurs qui codent en Visual Basic, elle l'est moins pour les programmeurs qui utilisent d'autres langages.

- Si vous avez un doute concernant une fonctionnalité RDS déterminée et que vous possédez certaines connaissances dans un autre langage, vous pouvez éventuellement résoudre votre problème en examinant cette même fonction exprimée dans un autre langage.

## <a name="how-the-tutorial-is-presented"></a>Présentation du didacticiel

Ce didacticiel est basé sur le modèle de programmation RDS. Chaque étape du modèle de programmation y est abordée, avec en outre une illustration de chacune de ces étapes par un fragment de code Visual Basic.

L'exemple de code est reproduit dans les autres langages avec un minimum de détails. Chaque étape figurant dans le didacticiel d'un langage de programmation donné s'accompagne d'une mention de l'étape correspondante dans le modèle de programmation et le didacticiel descriptif. Servez-vous du numéro de l'étape pour accéder aux détails correspondants dans le didacticiel descriptif.

Le modèle de programmation RDS est indiqué ci-dessous. Référez-vous-y à mesure que vous avancez dans le didacticiel.

## <a name="rds-programming-model-with-objects"></a>Modèle de programmation RDS avec des objets

- Spécifiez le programme à appeler sur le serveur et obtenir un moyen (proxy) d'y faire référence à partir du client.

- Appelez le programme serveur. Transmettez les paramètres au programme serveur qui identifie la source de données et la commande à émettre.

- Le programme serveur obtient un objet [Recordset](recordset-object-ado.md) auprès de la source de données, généralement en utilisant ADO. L'objet **Recordset** peut éventuellement être traité sur le serveur.

- Le programme serveur retourne l'objet **Recordset** final à l'application cliente.

- Au niveau du client, l'objet **Recordset** est éventuellement placé dans un format facilement exploitable par des contrôles visuels.

- Les modifications apportées à l'objet **Recordset** sont renvoyées au serveur et utilisées pour la mise à jour de la source de données.

Voici les étapes décrites dans ce didacticiel :

- [Étape 1 : Spécifier un programme serveur](step-1-specify-a-server-program-rds-tutorial.md)
- [Étape 2 : Appeler le programme serveur](step-2-invoke-the-server-program-rds-tutorial.md)
- [Étape 3 : Le serveur obtient un objet Recordset](step-3-server-obtains-a-recordset-rds-tutorial.md)
- [Étape 4 : Le serveur retourne l’objet Recordset](step-4-server-returns-the-recordset-rds-tutorial.md)
- [Étape 5 : L’objet DataControl est rendu utilisable](step-5-datacontrol-is-made-usable-rds-tutorial.md)
- [Étape 6 : Les modifications sont envoyées au serveur](step-6-changes-are-sent-to-the-server-rds-tutorial.md)
- [Didacticiel RDS (VBScript)](rds-tutorial-vbscript.md)
- [Didacticiel RDS (Visual J ++)](rds-tutorial-visual-j.md)