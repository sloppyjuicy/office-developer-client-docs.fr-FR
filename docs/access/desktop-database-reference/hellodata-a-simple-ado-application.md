---
title: 'HelloData : une application ADO simple'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7d9be9b91b3f847516eb3c22aa37e46c8a551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292019"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData : une application ADO simple

**S’applique à** : Access 2013, Office 2013

Pour jeter les bases de l'exploration de la bibliothèque ADO, prenons l'exemple d'une application ADO simple appelée « HelloData ». HelloData suit les quatre étapes principales des opérations ADO (obtention, examen, modification et mise à jour des données). Afin de se concentrer sur les points fondamentaux d'ADO et éviter toute complication du code, la gestion des erreurs sera réduite à sa plus simple expression dans cet exemple.

L'application interroge la base de données exemple Northwind incluse dans Microsoft SQL Server 2000.

**Pour exécuter HelloData**

1.  Créez un nouveau projet Visual Basic exécutable standard qui fait référence à la bibliothèque ADO 2.5.

2.  Créez quatre boutons de commande en haut du formulaire, en définissant les propriétés **Name** et **Caption** avec les valeurs indiquées dans le tableau ci-dessous.

3.  En dessous des boutons, ajoutez un **contrôle Microsoft DataGrid** (Msdatgrd.ocx). Le fichier msdatgrd. ocx est fourni avec Visual Basic et se trouve dans \\votre\\répertoire Windows \\system32\\ou Winnt system32. Pour ajouter le contrôle DataGrid à la Boîte à outils Visual Basic, sélectionnez **Composants** dans le menu **Projet**. Activez ensuite la case à cocher en regard de « Microsoft DataGrid Control 6.0 (SP3) (OLEDB) » et cliquez sur **OK**. Pour ajouter le contrôle au projet, faites glisser le contrôle DataGrid de la Boîte à outils vers le formulaire Visual Basic.

4.  Créez une **zone de texte** sur le formulaire en dessous de la grille et définissez ses propriétés comme indiqué dans le tableau. Lorsque vous avez terminé, le formulaire doit être identique à celui illustré dans la figure suivante.

5.  Enfin, copiez le code figurant dans le [code HelloData](hellodata-code.md) et collez-le dans la fenêtre de l'éditeur de code du formulaire. Appuyez sur **F5** pour exécuter le code.

> [!NOTE]
> [!REMARQUE] Dans l'exemple suivant, et dans ce guide, l'utilisateur « MyId » et le mot de passe « 123aBc » sont utilisés pour l'authentification auprès du serveur. Vous devrez remplacer ces valeurs par des informations d'authentification de connexion réelles pour votre serveur. Remplacez également la valeur « MyServer » par le nom de votre serveur.

Pour obtenir une description détaillée du code, consultez les [Détails de HelloData](hellodata-details.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de contrôle</p></th>
<th><p>Propriété</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Formulaire</p></td>
<td><p>Nom</p></td>
<td><p>Form1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Hauteur</p></td>
<td><p>6500</p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p>Largeur</p></td>
<td><p>6500</p></td>
</tr>
<tr class="even">
<td><p>Grille de données MS</p></td>
<td><p>Nom</p></td>
<td><p>grdDisplay1</p></td>
</tr>
<tr class="odd">
<td><p>TextBox</p></td>
<td><p>Nom</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Ligne</p></td>
<td><p>true</p></td>
</tr>
<tr class="odd">
<td><p>Bouton de commande</p></td>
<td><p>Nom</p></td>
<td><p>cmdGetData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Légende</p></td>
<td><p>Get Data</p></td>
</tr>
<tr class="odd">
<td><p>Bouton de commande</p></td>
<td><p>Nom</p></td>
<td><p>cmdExamineData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Légende</p></td>
<td><p>Examine Data</p></td>
</tr>
<tr class="odd">
<td><p>Bouton de commande</p></td>
<td><p>Nom</p></td>
<td><p>cmdEditData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Légende</p></td>
<td><p>Edit Data</p></td>
</tr>
<tr class="odd">
<td><p>Bouton de commande</p></td>
<td><p>Nom</p></td>
<td><p>cmdUpdateData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Légende</p></td>
<td><p>Update Data</p></td>
</tr>
</tbody>
</table>



