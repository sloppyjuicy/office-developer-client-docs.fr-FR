---
title: CopyObject, action de macro
TOCTitle: CopyObject macro action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 19e003f1576405d4bc36c8365603c7871e1541c4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565673"
---
# <a name="copyobject-macro-action"></a>CopyObject, action de macro

**S’applique à** : Access 2013, Office 2013

Utilisez l'action **CopierObjet** pour copier l'objet de base de données spécifié dans une autre base de données Access ou dans la même base ou projet Access mais sous un nouveau nom. Par exemple, vous pouvez copier ou enregistrer un objet existant dans une autre base de données ou créer rapidement un objet similaire en n'apportant que quelques modifications.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Paramètre

L’action **CopierObjet** possède les arguments suivants.

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
<td><p><strong>Base de données de destination</strong></p></td>
<td><p>Chemin d’accès valide et nom de fichier de la base de données de destination. Entrez le chemin d’accès et le nom de fichier dans la zone <strong>Base de données de destination</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Laissez cet argument vide si vous souhaitez sélectionner la base de données active. 

</p><p><strong>REMARQUE</strong>: cet argument est disponible uniquement dans l’environnement de base de données Access. Si cette action est utilisée dans un environnement de projet Access (.adp), l’argument Base de données de destination doit être vide.</p>
<p>Si vous exécutez une macro contenant l’action <strong>CopierObjet</strong> dans une base de données bibliothèque et que vous laissez cet argument vide, Microsoft Office Access 2007 copie l’objet dans la base de données bibliothèque.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nouveau nom</strong></p></td>
<td><p>Nouveau nom de l’objet. En cas de copie dans une base de données différente, laissez cet argument vide pour conserver le même nom.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type d’objet source</strong></p></td>
<td><p>Type d’objet à copier. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong>. Pour copier l’objet sélectionné dans le volet de navigation, laissez cet argument vide.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l’objet source</strong></p></td>
<td><p>Nom de l’objet à copier. La zone <strong>Nom de l’objet source</strong> affiche tous les objets de la base de données correspondant au type sélectionné par l’argument <strong>Type d’objet source</strong>. Dans la zone <strong>Nom de l’objet source</strong>, cliquez sur l’objet à copier. Si vous laissez l’argument <strong>Type d’objet source</strong> vide, laissez également celui-ci vide. Si vous exécutez une macro contenant l’action <strong>CopierObjet</strong> dans une base de données bibliothèque, Access commence par rechercher un objet portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous devez entrer une valeur pour l’argument **Base de données de destination** et/ou **Nouveau nom** pour cette action.

Si vous laissez les arguments **Type d'objet source** et **Nom de l'objet source** vides, Access copie l'objet sélectionné dans le volet de navigation. Pour sélectionner un objet dans le volet de navigation, vous pouvez utiliser l'action **SélectionnerObjet** avec l'argument DansVoletDeNavigation défini sur **Oui**.

L'action **CopierObjet** équivaut à réaliser les étapes suivantes manuellement :

1. Sélectionnez un objet dans le volet de navigation.

2. Sous l'onglet Home, dans le groupe Clipboard, cliquez sur Copy.

3. Sous le même onglet, cliquez sur **Coller**.La boîte de dialogue **Coller sous** s'affiche afin que vous puissiez donner un nouveau nom à l'objet. L'action **CopierObjet** effectue toutes ces étapes automatiquement.

> [!NOTE]
> [!REMARQUE] Lors de la copie des pages d'accès aux données, l'action **CopierObjet** copie uniquement le lien vers le fichier .htm associé, pas le fichier lui-même.

Le chemin d'accès et le nom de fichier de la base de données de destination doivent exister préalablement à l'exécution de l'action **CopierObjet** par la macro. S'ils n'existent pas, Access affiche un message d'erreur.

Pour exécuter l'action **CopierObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **CopyObject** de l'objet **DoCmd**.

Vous pouvez également copier manuellement un objet sélectionné dans le volet de navigation ou un objet qui est actuellement ouvert en cliquant sur l'onglet **Fichier**, puis sur **Enregistrer sous**. Cette commande fait une copie de l'objet dans la base de données active uniquement. Dans la boîte de dialogue **Enregistrer sous**, entrez le nom de la copie et choisissez le type d'objet sous lequel vous voulez l'enregistrer. Si l'objet d'origine a déjà été enregistré et que vous l'enregistrez dans la base de données active sous un nouveau nom, la version d'origine est conservée sous son ancien nom.

Pour copier manuellement un objet dans une base de données Access différente :

1. Sous l'onglet **Données externes**, dans le groupe **Exporter**, cliquez sur **Autres**, puis cliquez sur **Base de données Access**.

2. Dans la boîte de dialogue **Exportation - Base de données Access**, entrez le nom de fichier de la base de données de destination.- ou -Cliquez sur **Parcourir** pour afficher la boîte de dialogue **Enregistrer**, recherchez la base de données de destination, puis cliquez sur **Enregistrer**.

3. Dans la boîte de dialogue **Exportation - Base de données Access**, cliquez sur **OK**. La boîte de dialogue **Exporter** s'affiche.

4. Dans la boîte de dialogue **Exporter**, entrez le nom de l'objet dans la base de données de destination. Choisissez les options appropriées, comme **Définition et données** ou **Définition uniquement** pour les tables. Lorsque vous avez terminé, cliquez sur **OK**.

