---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36d7bf1b39186eca841e417473e31e2bfd3a2dfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469549"
---
# <a name="using-the-command-object-access"></a>Using the Command Object (Access)


**S’applique à**: Access 2013 | Office 2013

Une fois connecté à une source de données, vous devez y exécuter des requêtes pour obtenir des jeux de résultats. ADO encapsule ce type de fonctionnalité de commande dans l'objet **Command**.

Vous pouvez utiliser l'objet **Command** pour demander au fournisseur n'importe quel type d'opération, à condition que ce dernier puisse interpréter correctement la chaîne de commande. Une des opérations courantes pour les fournisseurs de données est l'interrogation d'une base de données et le renvoi des enregistrements correspondants dans un objet **Recordset**. Les objets **Recordset** seront présentés plus loin dans ce chapitre et dans d'autres chapitres. Considérons-les pour l'instant comme des outils permettant de stocker et d'afficher des jeux de résultats. Comme pour un certain nombre d'objets ADO, selon les fonctionnalités offertes par le fournisseur, la référence à certaines collections, méthodes ou propriétés de l'objet **Command** peut générer des erreurs.

Il n'est pas toujours nécessaire de créer un objet **Command** pour exécuter une commande sur une source de données. Vous pouvez utiliser la méthode **Execute** sur l'objet **Connection**, ou la méthode **Open** sur l'objet **Recordset**. Toutefois, vous devez impérativement utiliser un objet **Command** si vous devez réutiliser une commande dans votre code ou si vous devez transmettre des informations de paramétrage avec votre commande. Ces scénarios sont présentés en détail dans une autre section du présent chapitre.


> [!NOTE]
> <P>Certains objets <STRONG>Command</STRONG> peuvent renvoyer un jeu de résultats sous la forme d’un flux binaire ou d’un objet <STRONG>Record</STRONG> unique, plutôt que sous forme d’un objet <STRONG>Recordset</STRONG>, si le fournisseur le prend en charge. En outre, certains objets <STRONG>Command</STRONG> ne sont pas conçus pour renvoyer de jeu de résultats (par exemple, une requête SQL Update). Ce chapitre présente le scénario le plus courant, c’est-à-dire l’exécution d’objets <STRONG>Command</STRONG> renvoyant ses résultats dans un objet <STRONG>Recordset</STRONG>. Pour plus d’informations sur le renvoi de résultats dans les objets <STRONG>Recordset</STRONG> ou <STRONG>Stream</STRONG>,  consultez le <A href="chapter-10-records-and-streams.md">Chapitre 10 : Enregistrements et flux</A>.</P>


