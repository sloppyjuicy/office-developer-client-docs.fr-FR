---
description: Filter, propriété
title: Filter, propriété (ADO)
TOCTitle: Filter property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b15abbd02ee91013f6ec2d52c88554d1a4f80d96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626546"
---
# <a name="filter-property-ado"></a>Filter, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le filtre utilisé pour les données d'un [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur **Variant** qui peut l'une des valeurs suivantes :

  - **Chaîne de critères**: chaîne constituée d'une ou plusieurs clauses individuelles concaténées avec les opérateurs **AND** ou **OR**.

  - **Tableau de signets**: tableau de valeurs de signets uniques pointant vers des enregistrements de l'objet **Recordset**.

  - Valeur [FilterGroupEnum](filtergroupenum.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **Filter** pour filtrer les enregistrements d’un objet **Recordset**. Le **Recordset** filtré devient le curseur actuel. Les autres propriétés qui renvoient des valeurs dépendant du curseur actuel sont affectées (par exemple [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [CpteEnregistrement](recordcount-property-ado.md) et [ComptePage](pagecount-property-ado.md)). Cela est dû au fait que l’attribution d’une valeur spécifique à la propriété **Filter** déplace l’enregistrement actuel et le définit comme le premier enregistrement satisfaisant la nouvelle valeur.

La chaîne de critères est composé de clauses au formulaire *FieldName-Operator-Value* (par exemple, « LastName = ' Smith »). Vous pouvez créer des clauses composées en concatenant des clauses individuelles avec **AND** (par exemple, « LastName = 'Smith' AND FirstName = 'John' ») ou **OR** (par exemple, « ). Vous pouvez créer des clauses composées en concatenant des clauses individuelles avec **AND** (par exemple, « LastName = 'Smith' AND FirstName = 'John' ») ou **OR** (par exemple, « LastName = 'Smith' OR LastName = 'Jones' »). Lorsque vous utilisez des chaînes de critères, gardez les points suivants à l’esprit :

  - *NomChamp* doit être un nom de champ valide du **Recordset**. Si le nom de champ contient des espaces, vous devez le mettre entre crochets.

  - *L’opérateur* doit être l’un des suivants \<, \> : , \<=, \> =, , = ou \<\> **LIKE**.

  - *La* valeur est la valeur à laquelle vous comparerez les valeurs de champ (par exemple, « Smith » \# 8/24/95, \# 12,345 ou 50,00 $). Utilisez des guillemets simples avec des chaînes et des signes de livre \# () avec des dates. Pour les chiffres, vous pouvez utiliser des virgules, des signes dollar et des symboles mathématiques. Si l’*Operateur* est **LIKE**, la *Valeur* peut contenir des caractères génériques. Seuls l’astérisque () et le signe pourcentage (%) sont autorisés et doivent être le \* dernier caractère de la chaîne. La *Valeur* ne peut pas être nulle.

    > [!NOTE]
    > [!REMARQUE] Pour insérer des guillemets simples (') dans la valeur Value du filtre, utilisez deux guillemets simples pour en représenter un. Par exemple, pour créer un filtre O'Malley, la chaîne de critères doit être « col1 = 'O''Malley' ». Pour insérer des guillemets simples au début et à la fin de la valeur du filtre, placez un signe dièse (#) devant et derrière la chaîne. Par exemple, pour filtrer la valeur '1', la chaîne de critères doit apparaître ainsi « col1 = #'1'# ».

-   Il n'y a aucune priorité entre **AND** et **OR**. Les clauses peuvent être regroupées entre parenthèses. Toutefois, vous ne pouvez pas grouper des clauses jointes par un **ou,** puis joindre le groupe à une autre clause avec **un AND,** comme dans l’extrait de code suivant :  
 `(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'`  
  
-   Construisez plutôt ce filtre de la façon suivante :  
 `(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John')`  

  - Dans une clause **LIKE,** vous pouvez utiliser un caractère générique au début et à la fin du modèle (par exemple, LastName Like ' mit '), ou uniquement à la fin du modèle \* \* (par exemple, LastName Like 'Smit \* ').

Les constantes de filtre facilitent la résolution des conflits d'enregistrement ponctuels lors des mises à jour par lot en vous permettant d'afficher, par exemple, uniquement les enregistrements concernés par le dernier appel de la méthode [UpdateBatch](updatebatch-method-ado.md).

La définition de la propriété **Filter** à proprement parler peut échouer en raison d'un conflit avec les données sous-jacentes (par exemple si l'enregistrement a déjà été supprimé par un autre utilisateur). Dans ce cas, le fournisseur renvoie des avertissements vers la collection [Errors](errors-collection-ado.md), mais n'arrête pas d'exécution de programme. Une erreur d'exécution n'est générée que s'il existe des conflits sur tous les enregistrements demandés. Utilisez la propriété [Status](status-property-ado-recordset.md) pour localiser les enregistrements générant des conflits.

L'attribution d'une chaîne vide à la propriété **Filter** ("") a le même effet que l'utilisation de la constante **adFilterNone**.

Lorsque la propriété **Filter** est définie, la position de l'enregistrement actuel se déplace vers le premier enregistrement du sous-ensemble d'enregistrements filtré du **Recordset**. De même, quand la propriété **Filter** est effacée, la position d'enregistrement actuel passe au premier enregistrement du **Recorset**.

Pour plus d'explications sur les valeurs de signets à partir desquelles vous pourrez construire un tableau utilisable avec la propriété [Filter](bookmark-property-ado.md), voir la propriété **Bookmark**.

**Seuls** les filtres sous la forme de chaînes de critères (par exemple, OrderDate \> '31/12/1999') affectent le contenu d’un **recordset persistant.** Les **filtres** créés avec un tableau de **signets** ou en utilisant une valeur provenant de **FilterGroupEnum** ne modifient pas le contenu du jeu d'enregistrements persistant. Ces règles s'appliquent aux **jeux d'enregistrements** créés avec des curseurs côté client ou côté serveur.

> [!NOTE]
> [!REMARQUE] Lorsque vous appliquez l'indicateur **adFilterPendingRecords** à un **jeu d'enregistrements** filtré et modifié lors d'une mise à jour par lot, le **jeu d'enregistrements** résultant est vide si le filtrage portait sur le champ clé d'une table à clé unique et si la modification a été apportée sur les valeurs de ce champ clé. Le **jeu d'enregistrements** résultant n'est pas vide si l'une des affirmations suivantes est vraie :
> - Le filtrage portait sur des champs non-clé d'une table à clé unique.
> - Le filtrage portait sur l'un des champs d'une table à clés multiples.
> - Les modifications ont été apportées sur des champs non-clés d'une table à clé unique.
> - Les modifications ont été apportées sur l'un des champs d'une table à clés multiples.

Le tableau suivant résume les effets d' **adFilterPendingRecords** dans différentes combinaisons de filtrage et de modifications. La colonne de gauche indique les modifications possibles ; les modifications peuvent être apportées sur tous les champs non-clés, sur le champ clé d'une table à clé unique ou l'un des champs clé d'une table à clés multiples. La ligne supérieure indique le critère de filtrage ; le filtrage peut porter sur l'un des champs non-clés, sur le champ clé d'une table à clé unique ou sur n'importe lequel des champs clé d'une table à clés multiples. Les cellules qui se recoupent présentent les résultats : + signifie que l'application de **adFilterPendingRecords** donne un **Recordset** non vide ; **-** indique un **Recordset** vide.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p>Non-clés</p></th>
<th><p>Clé unique</p></th>
<th><p>Clés multiples</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Non-clés</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p>Clé unique</p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="odd">
<td><p>Clés multiples</p></td>
<td><p>+</p></td>
<td><p>S/O</p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>

