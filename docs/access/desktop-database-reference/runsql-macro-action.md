---
title: RunSQL, action de macro
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f3ef598ad50747d99ca884043e03ebfabfef8f63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308994"
---
# <a name="runsql-macro-action"></a>RunSQL, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l'action **ExécuterSQL** pour exécuter une requête Action Access en utilisant l'instruction SQL correspondante. Vous pouvez également utiliser une requête Définition des données.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Paramètre

L’action **ExécuterSQL** accepte les arguments suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Instruction SQL</strong></p></td>
<td><p>Instruction SQL pour la requête Action ou Définition des données que vous souhaitez exécuter. L'instruction peut compter au maximum 255 caractères. Cet argument est obligatoire.</p></td>
</tr>
<tr class="even">
<td><p><strong>Utilise la transaction</strong></p></td>
<td><p>Sélectionnez <strong>Oui</strong> pour inclure cette requête dans une transaction. Choisissez <strong>Non</strong> si vous ne souhaitez pas utiliser de transaction. La valeur par défaut est <strong>Oui</strong>. Si vous sélectionnez la valeur <strong>Non</strong> pour cet argument, l'exécution de la requête peut être plus rapide.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser des requêtes Action pour ajouter, supprimer ou mettre à jour des enregistrements et pour enregistrer le jeu de résultats d'une requête en tant que nouvelle table. Vous pouvez utiliser des requêtes Définition des données pour créer, modifier et supprimer des tables ou encore pour créer et supprimer des index. Avec l'action **ExécuterSQL**, vous pouvez effectuer ces opérations directement à partir d'une macro sans devoir utiliser les requêtes stockées.

Si vous devez spécifier une instruction SQL comportant plus de 255 caractères, utilisez plutôt la méthode **RunSQL** de l'objet **DoCmd** dans un module Visual Basic pour Applications (VBA). Vous pouvez taper des instructions SQL comptant jusqu'à 32 768 caractères dans VBA.

Les requêtes Access sont en fait des instructions SQL créées lorsque vous créez une requête à l'aide de la grille de création dans la fenêtre Requête. Le tableau suivant répertorie les requêtes Action et Définition des données d'Access et leurs instructions SQL correspondantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de requête</p></th>
<th><p>Instruction SQL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Action</strong></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Ajout</p></td>
<td><p>INSERT INTO</p></td>
</tr>
<tr class="odd">
<td><p>Suppression</p></td>
<td><p>DELETE</p></td>
</tr>
<tr class="even">
<td><p>Création de table</p></td>
<td><p>Sélectionnez... VERS</p></td>
</tr>
<tr class="odd">
<td><p>Mise à jour</p></td>
<td><p>UPDATE</p></td>
</tr>
<tr class="even">
<td><p><strong>Définition de données (spécifique SQL)</strong></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer une table</p></td>
<td><p>CREATE TABLE</p></td>
</tr>
<tr class="even">
<td><p>Modifier une table</p></td>
<td><p>ALTER TABLE</p></td>
</tr>
<tr class="odd">
<td><p>Supprimer une table</p></td>
<td><p>DROP TABLE</p></td>
</tr>
<tr class="even">
<td><p>Créer un index</p></td>
<td><p>CREATE INDEX</p></td>
</tr>
<tr class="odd">
<td><p>Supprimer un index</p></td>
<td><p>DROP INDEX</p></td>
</tr>
</tbody>
</table>

Vous pouvez également utiliser une clause IN avec ces instructions pour modifier des données dans une autre base de données.

> [!NOTE]
> [!REMARQUE] Pour exécuter une requête Sélection ou une requête Analyse croisée à partir d'une macro, utilisez l'argument Affichage de l'action **OuvrirRequête** pour ouvrir une requête Sélection ou Analyse croisée existante en mode Feuille de données. Vous pouvez également exécuter des requêtes Action et des requêtes spécifiques SQL existantes de la même façon.
