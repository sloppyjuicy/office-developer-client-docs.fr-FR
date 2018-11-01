---
title: Action de Macro ShowAllRecords
TOCTitle: ShowAllRecords Macro Action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b6482bcd34562e13e1783f8e0702718eeaed0b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881733"
---
# <a name="showallrecords-macro-action"></a>Action de Macro ShowAllRecords


**S’applique à**: Access 2013, Office 2013


Vous pouvez utiliser l’action **AfficherTousEnreg** pour supprimer n’importe quel filtre appliqué à la table active, le jeu de résultats de requête ou le formulaire et afficher tous les enregistrements dans l’ensemble de la table ou les résultats ou tous les enregistrements dans la table sous-jacente du formulaire ou de la requête.

## <a name="setting"></a>Paramètre

L’action **AfficherTousEnreg** ne possède aucun argument.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette action pour vous assurer que tous les enregistrements (y compris les enregistrements modifiés ou nouveaux) d’une table, un jeu de résultats de requête ou un formulaire sont affichés. Cette action entraîne une actualisation des enregistrements pour un formulaire ou un sous-formulaire.

Vous pouvez également utiliser cette action pour supprimer n’importe quel filtre appliqué avec l’action **AppliquerFiltre** , la commande **filtrer** sous l’onglet **accueil** , ou le **Nom du filtre** ou l’argument **Condition Where** de l’action **OuvrirFormulaire** .

Cette action a le même effet qu’en cliquant sur **Basculer le filtre** sous l’onglet **accueil** , ou cliquez sur le champ filtré et cliquez sur **Effacer le filtre de...** en mode formulaire, en mode ou mode feuille de données.

Pour exécuter l’action **AfficherTousEnreg** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **ShowAllRecords** de l’objet **DoCmd** .

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
<td><p>[Filtres nom société] = 1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condition Where</strong>: [nom de société] comme &quot;[AÀÁÂÃÄ] *&quot;</p></td>
<td><p>Filtre les noms de sociétés commençant par A, À, Á, Â, Ã ou Ä.</p></td>
</tr>
<tr class="even">
<td><p>[Filtres nom société] = 2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condition Where</strong>: [nom de société] comme &quot;B *&quot;</p></td>
<td><p>Filtre les noms de sociétés commençant par B.</p></td>
</tr>
<tr class="odd">
<td><p>[Filtres nom société] = 3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condition Where</strong>: [nom de société] comme &quot;[CÇ] *&quot;</p></td>
<td><p>Filtre les noms de sociétés commençant par C ou Ç.</p></td>
</tr>
<tr class="even">
<td><p>... Les lignes d’action pour les lettres D à Y ont le même format que pour les lettres A à C ...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Filtres nom société] = 26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condition Where</strong>: [nom de société] comme &quot;[ZÆØÅ] *&quot;</p></td>
<td><p>Filtre les noms de sociétés commençant par Z, Æ, Ø ou Å.</p></td>
</tr>
<tr class="even">
<td><p>[Filtres nom société] = 27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Affiche tous les enregistrements</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. [RecordCount] &gt;0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: NomSociété</p></td>
<td><p>Si des enregistrements sont renvoyés pour la lettre sélectionnée, déplace le focus sur le contrôle NomSociété.</p></td>
</tr>
</tbody>
</table>

