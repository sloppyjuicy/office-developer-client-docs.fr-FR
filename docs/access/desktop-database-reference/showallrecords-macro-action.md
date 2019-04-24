---
title: ShowAllRecords, action de macro
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308644"
---
# <a name="showallrecords-macro-action"></a>ShowAllRecords, action de macro


**S’applique à** : Access 2013, Office 2013


Vous pouvez utiliser l'action **AfficherTousEnreg** pour supprimer tout filtre appliqué de la table active, du jeu de résultats de la requête ou du formulaire, et afficher tous les enregistrements de la table ou du jeu de résultats, ou tous les enregistrements de la table ou de la requête sous-jacente du formulaire.

## <a name="setting"></a>Setting

L'action **AfficherTousEnreg** ne possède aucun argument.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette action pour vous assurer que tous les enregistrements (y compris les enregistrements modifiés ou nouveaux) sont affichés pour une table, un jeu de résultats de requête ou un formulaire. Cette action entraîne une rérogation des enregistrements d'un formulaire ou d'un sous-formulaire.

Vous pouvez également utiliser cette action pour supprimer un filtre appliqué à l'aide de l'action **AppliquerFiltre** , de la commande **filtre** de l'onglet **Accueil** ou de l'argument **nom du filtre** ou **condition WHERE** de l'action **OuvrirFormulaire** .

Cette action équivaut à cliquer sur basculer le **filtre** sous l'onglet **Accueil** , ou à cliquer avec le bouton droit sur le champ filtré, puis à cliquer sur **effacer le filtre de...** en mode formulaire, en mode page ou en mode feuille de type de base de type.

Pour exécuter l'action **AfficherTousEnreg** dans un module Visual Basic pour applications (VBA), utilisez la méthode **ShowAllRecords** de l'objet **DoCmd** .

## <a name="example"></a>Exemple

**Appliquer un filtre à l'aide d'une macro**

La macro suivante contient un ensemble d'actions, chacune filtrant les enregistrements d'un formulaire Répertoire téléphonique clients. Elle illustre l'utilisation des actions **AppliquerFiltre**, **AfficherTousEnreg** et **AtteindreContrôle**. Elle montre également l'utilisation de conditions pour déterminer quel bouton bascule d'un groupe d'options a été sélectionné sur le formulaire. Chaque ligne d'action est associée à un bouton bascule qui sélectionne le jeu d'enregistrements commençant par A, B, C, etc., ou tous les enregistrements. Cette macro doit être attachée à l'événement **AprèsMAJ** du groupe d'options FiltresNomsSociétés.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Action</p></th>
<th><p>Arguments : Paramètre</p></th>
<th><p>Commentaire</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Filtres de nom de société] = 1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condition WHERE</strong>: [nom de la société &quot;] comme [AÀÁÂÃÄ] *&quot;</p></td>
<td><p>Filtre les noms de sociétés commençant par A, À, Á, Â, Ã ou Ä.</p></td>
</tr>
<tr class="even">
<td><p>[Filtres de nom de société] = 2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condition WHERE</strong>: [nom de la société &quot;] comme B *&quot;</p></td>
<td><p>Filtre les noms de sociétés commençant par B.</p></td>
</tr>
<tr class="odd">
<td><p>[Filtres de nom de société] = 3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condition WHERE</strong>: [nom de la société &quot;] comme [CÇ] *&quot;</p></td>
<td><p>Filtre les noms de sociétés commençant par C ou Ç.</p></td>
</tr>
<tr class="even">
<td><p>... Les lignes d’action pour les lettres D à Y ont le même format que pour les lettres A à C ...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Filtres de nom de société] = 26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condition WHERE</strong>: [nom de la société &quot;] comme [ZÆØÅ] *&quot;</p></td>
<td><p>Filtre les noms de sociétés commençant par Z, Æ, Ø ou Å.</p></td>
</tr>
<tr class="even">
<td><p>[Filtres de nom de société] = 27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Affiche tous les enregistrements</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. RecordCount &gt;0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: NomSociété</p></td>
<td><p>Si des enregistrements sont renvoyés pour la lettre sélectionnée, déplace le focus sur le contrôle NomSociété.</p></td>
</tr>
</tbody>
</table>

