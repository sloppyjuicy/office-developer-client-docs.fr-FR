---
title: Command, objet (ADO)
TOCTitle: Command Object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5199037f44e75bddf697197bca992a95b8432420
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605743"
---
# <a name="command-object-ado"></a>Command, objet (ADO)


**S’applique à**: Access 2013 | Office 2013

Définit une commande spécifique que vous avez l'intention d'exécuter sur une source de données.

## <a name="remarks"></a>Notes

Utilisez un objet **Command** pour interroger une base de données et renvoyer des enregistrements dans un objet [Recordset](recordset-object-ado.md), pour exécuter une opération en bloc ou pour manipuler la structure d'une base de données. Selon les fonctionnalités proposées par le fournisseur, certaines collections, méthodes ou propriétés **Command** risquent de générer une erreur lorsqu'elles sont référencées.

Les collections, les méthodes et les propriétés d'un objet **Command** vous permettent d'effectuer diverses tâches :

  - définir le texte exécutable de la commande (par exemple, une instruction SQL) avec la propriété [CommandText](commandtext-property-ado.md) ;

  - Définir des requêtes paramétrées ou des arguments de procédure stockée à l'aide des objets [Parameter](parameter-object-ado.md) et de la collection [Parameters](parameters-collection-ado.md).

<<<<<<< Tête
  - exécuter une commande et renvoyer le cas échéant un objet **Recordset** avec la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) ;
=======
  - exécuter une commande et renvoyer le cas échéant un objet **Recordset** avec la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) ;
>>>>>>> master

  - spécifier le type de commande avec la propriété [CommandType](commandtype-property-ado.md) avant exécution afin d'optimiser les performances ;

  - vérifier que le fournisseur enregistre une version préparée (compilée) de la commande avant exécution avec la propriété [Prepared](prepared-property-ado.md) ;

  - définir le nombre de secondes pendant lesquelles un fournisseur attendra qu'une commande s'exécute avec la propriété [CommandTimeout](commandtimeout-property-ado.md) ;

  - associer une connexion ouverte à un objet **Command** en définissant sa propriété [ActiveConnection](activeconnection-property-ado.md) ;

  - définir la propriété [Name](name-property-ado.md) pour identifier l'objet **Command** en tant que méthode pour l'objet [Connection](connection-object-ado.md) associé ;

  - passer un objet **Command** à la propriété [Source](source-property-ado-recordset.md) d'un objet **Recordset** afin d'obtenir des données ;

  - accéder aux attributs spécifiques du fournisseur avec la collection [Properties](properties-collection-ado.md).


> [!NOTE]
> <P>[!REMARQUE] Pour exécuter une requête sans utiliser d'objet <STRONG>Command</STRONG>, passez une chaîne de requête à la méthode <A href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</A> d'un objet <STRONG>Connection</STRONG> ou à la méthode <A href="open-method-ado-recordset.md">Open</A> d'un objet <STRONG>Recordset</STRONG>. Toutefois, un objet <STRONG>Command</STRONG> est nécessaire si vous voulez rendre persistant le texte de commande et l'exécuter de nouveau, ou utiliser des paramètres de requête.</P>



Pour créer un objet **Command** indépendamment d'un objet **Connection** déjà défini, définissez sa propriété **ActiveConnection** sur une chaîne de connexion valide. ADO crée tout de même un objet **Connection**, mais il ne l'affecte pas à une variable objet. Toutefois, si vous associez plusieurs objets **Command** à la même connexion, vous devez créer et ouvrir explicitement un objet **Connection**; l'objet **Connection** est ainsi affecté à une variable objet. Si vous ne définissez pas la propriété **ActiveConnection** de l'objet **Connection** avec cette variable objet, ADO crée un nouvel objet **Connection** pour chaque objet **Command**, même si vous utilisez la même chaîne de connexion.

Pour exécuter un objet **Command**, il vous suffit de l'appeler à l'aide de sa propriété [Name](name-property-ado.md) sur l'objet **Connection** associé. La propriété **ActiveConnection** de **Command** doit être définie sur l'objet **Connection**. Si **Command** possède des paramètres, passez ses valeurs en tant qu'arguments à la méthode.

Si deux objets **Command** ou plus sont exécutés sur la même connexion et que l'un d'eux**** est une procédure stockée sans paramètres de sortie, une erreur se produit. Pour exécuter chaque objet **Command**, utilisez des connexions distinctes ou déconnectez tous les autres objets **Command**.

La collection **Parameters** est le membre par défaut de l'objet **Command**. Les deux instructions suivantes sont donc équivalentes.

