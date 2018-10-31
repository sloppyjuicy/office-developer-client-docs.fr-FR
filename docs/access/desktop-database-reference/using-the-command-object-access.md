---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1779f2c7e16e2f39a3912f271296c6a7bd0fd550
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861945"
---
# <a name="using-the-command-object-access"></a>Using the Command Object (Access)


**S’applique à**: Access 2013 | Office 2013

Une fois connecté à une source de données, vous devez y exécuter des requêtes pour obtenir des jeux de résultats. ADO encapsule ce type de fonctionnalité de commande dans l'objet **Command**.

Vous pouvez utiliser l'objet **Command** pour demander au fournisseur n'importe quel type d'opération, à condition que ce dernier puisse interpréter correctement la chaîne de commande. Une des opérations courantes pour les fournisseurs de données est l'interrogation d'une base de données et le renvoi des enregistrements correspondants dans un objet **Recordset**. Les objets **Recordset** seront présentés plus loin dans ce chapitre et dans d'autres chapitres. Considérons-les pour l'instant comme des outils permettant de stocker et d'afficher des jeux de résultats. Comme pour un certain nombre d'objets ADO, selon les fonctionnalités offertes par le fournisseur, la référence à certaines collections, méthodes ou propriétés de l'objet **Command** peut générer des erreurs.

Il n'est pas toujours nécessaire de créer un objet **Command** pour exécuter une commande sur une source de données. Vous pouvez utiliser la méthode **Execute** sur l'objet **Connection**, ou la méthode **Open** sur l'objet **Recordset**. Toutefois, vous devez impérativement utiliser un objet **Command** si vous devez réutiliser une commande dans votre code ou si vous devez transmettre des informations de paramétrage avec votre commande. Ces scénarios sont présentés en détail dans une autre section du présent chapitre.

> [!NOTE]
> Certaines commandes peuvent renvoyer un résultat sous forme de flux binaire ou en tant qu’un seul enregistrement au lieu d’un jeu d’enregistrements, si cela est pris en charge par le fournisseur. En outre, certaines commandes ne sont pas destinés à renvoyer de jeu de résultats (par exemple, une requête SQL Update). Ce chapitre présente le scénario le plus courant, toutefois : exécution des commandes qui retournent des résultats dans un objet Recordset. Pour plus d’informations sur le renvoi des résultats en enregistrements ou en flux, voir [chapitre 10 : enregistrements et flux](chapter-10-records-and-streams.md).

Cette section comprend les rubriques suivantes :

- [Vue d’ensemble de l’objet Command](command-object-overview.md)

- [Création et exécution d’une commande simple](creating-and-executing-a-simple-command.md)

- [Paramètres de l’objet Command](command-object-parameters.md)

- [Appel d’une procédure stockée à l’aide d’une commande](calling-a-stored-procedure-with-a-command.md)

- [Commandes nommées](named-commands.md)
