---
title: ExportWithFormatting, action de macro
TOCTitle: ExportWithFormatting macro action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 41c2be7b412bf043f392fb5d26ba5eb2cbc9971c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606778"
---
# <a name="exportwithformatting-macro-action"></a>ExportWithFormatting, action de macro


**S’applique à** : Access 2013, Office 2013

Faites appel à l’action **ExporterAvecMiseEnForme** pour sortir les données dans l’objet de base de données Microsoft Access spécifié (une feuille de données, un formulaire, un état, un module, une page d’accès aux données) dans des formats de sortie différents.

## <a name="settings"></a>Paramètres

L’action **ExporterAvecMiseEnForme** utilise les arguments suivants :

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
<td><p><strong>Type d’objet</strong></p></td>
<td><p>Type d’objet contenant les données à copier. Cliquez sur <strong>Table</strong> (pour une feuille de données de table), <strong>Requête</strong> (pour une feuille de données de requête), <strong>Formulaire</strong> (pour un formulaire ou une feuille de données de formulaire), <strong>État</strong>, <strong>Module</strong>, <strong>Vue serveur</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet du Générateur de macro. Vous ne pouvez pas copier une macro. Pour copier l’objet actif, sélectionnez son type à l’aide de cet argument et laissez l’argument <strong>Nom de l’objet</strong> vide. Cet argument est obligatoire. La valeur par défaut est <strong>Table</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l’objet</strong></p></td>
<td><p>Nom de l'objet contenant les données à créer. La zone <strong>Nom de l'objet</strong> regroupe tous les objets de la base de données ayant le type sélectionné par l'argument <strong>Type d'objet</strong>. Si vous exécutez une macro contenant l'action <strong>ExportWithFormatting</strong> dans une base de données bibliothèque, Access recherche d'abord l'objet portant ce nom dans la base de données bibliothèque, puis dans la base de données active.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Format de sortie</strong></p></td>
<td><p>Type de format à utiliser pour la copie des données. Vous avez le choix entre <strong>Classeur Excel 97-2003 (*.xls)</strong>, <strong>Classeur binaire Excel (*.xlsb)</strong>, <strong>Classeur Excel (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Classeur Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>Format PDF (*.pdf)</strong>, <strong>Format RTF (*.rtf)</strong>, <strong>Fichiers texte (*.txt)</strong> et <strong>Format XPS (*.xps)</strong>. Si vous laissez cet argument vide, Access vous demande de spécifier le format de sortie.</p></td>
</tr>
<tr class="even">
<td><p><strong>Fichier de copie</strong></p></td>
<td><p>Fichier dans lequel vous souhaitez copier les données, incluant le chemin complet. Vous pouvez inclure l’extension de nom de fichier classique pour le format de copie sélectionné avec l’argument <strong>Format de copie</strong>, mais cela n’est pas obligatoire. Si vous ne renseignez pas l’argument <strong>Fichier de copie</strong>, Access vous invite à indiquer un nom de fichier de copie.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Lancement auto</strong></p></td>
<td><p>Spécifie si le logiciel approprié doit se lancer immédiatement après l’exécution de l’action <strong>ExporterAvecMiseEnForme</strong>, avec le fichier spécifié par l’argument <strong>Fichier de copie</strong> ouvert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Fichier modèle</strong></p></td>
<td><p>Chemin d’accès et nom de fichier du fichier à utiliser comme modèle pour les fichiers HTML. Le fichier de modèle est un fichier texte qui comporte des balises HTML et des jetons propres à Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Encodage</strong></p></td>
<td><p>Type de format de chiffrement des caractères voulu pour le texte ou les données HTML à copier. Vous avez le choix entre <strong>MS-DOS</strong>, <strong>Unicode</strong> et <strong>Unicode (UTF-8)</strong>. Le paramètre de l’argument <strong>MS-DOS</strong> n’est disponible que pour les fichiers texte. Si vous laissez cet argument vide, Access copie les données avec l’encodage Windows par défaut pour les fichiers texte et avec l’encodage système par défaut pour les fichiers HTML.</p></td>
</tr>
<tr class="even">
<td><p><strong>Qualité de copie</strong></p></td>
<td><p>Sélectionnez <strong>Imprimer</strong> pour optimiser la copie d’impression ou <strong>Écran</strong> pour optimiser la copie à afficher à l’écran.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Les données Access sont copiées dans le format sélectionné et peuvent être lues par tout programme qui utilise ce format. Par exemple, vous pouvez copier un état Access avec sa mise en forme vers un document RTF et ouvrir ensuite ce document dans Microsoft Word.

Si vous copiez l’objet de base de données au format HTML, Access crée un fichier HTML contenant les données de l’objet. Vous pouvez utiliser l’argument **Fichier de modèle** pour spécifier un fichier à utiliser comme modèle pour le fichier .html.

Les règles suivantes s’appliquent lorsque vous utilisez l’action **ExporterAvecMiseEnForme** pour copier un objet de base de données dans l’un des formats de copie :

  - Vous pouvez copier des données dans une table, une requête et des feuilles de données de formulaire. Dans le fichier de copie, tous les champs de la feuille de données apparaissent comme dans Access, à l’exception des champs contenant des objets OLE. Les colonnes des champs des objets OLE sont incluses dans le fichier de copie, mais sont vides.

  - Dans le cas d'un contrôle lié à un champ Oui/Non (un bouton bascule, une case d'option ou une case à cocher), le fichier de copie affiche la valeur -1 (Oui) ou 0 (Non).

  - Dans le cas d’une zone de texte liée à un champ de lien hypertexte, le fichier de copie affiche le lien hypertexte pour tous les formats de sortie excepté le format texte MS-DOS (dans ce cas, le lien hypertexte s’affiche en tant que texte normal).

  - Si vous copiez les données dans un formulaire en mode Formulaire, le fichier de copie contient la vue de feuille de données de ce formulaire.

  - Lorsque vous copiez une feuille de données, un formulaire ou une page d’accès aux données au format HTML, un fichier .html est créé et lorsque vous copiez un état au format HTML, un fichier .html est créé pour chaque page de l’état.

Le résultat de l’exécution de l’action **ExporterAvecMiseEnForme** équivaut à cliquer sur une des options du groupe **Export** de l’onglet **Données externes**. Les arguments de l’action correspondent aux paramètres de la boîte de dialogue **Exporter**.

Pour exécuter l’action **ExporterAvecMiseEnForme** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OutputTo** de l’objet **DoCmd**.

