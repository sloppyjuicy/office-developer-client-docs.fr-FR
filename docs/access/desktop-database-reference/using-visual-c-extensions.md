---
title: Utilisation des extensions Visual C++
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8bf2234e5935c2a1a13871e7e45c980fb9f33109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312060"
---
# <a name="using-visual-c-extensions"></a>Utilisation d’extensions Visual C++


**S’applique à** : Access 2013, Office 2013

## <a name="the-iadorecordbinding-interface"></a>Interface IADORecordBinding

Les extensions Microsoft Visual C++ pour ADO associent, ou lient, des champs d'un objet [Recordset](recordset-object-ado.md) à des variables C/C++. Chaque fois que la ligne active de l'objet **Recordset** lié est modifiée, tous les champs liés de l'objet **Recordset** sont copiés dans les variables C/C++. Si nécessaire, les données copiées sont converties dans le type de données déclaré de la variable C/C++.

La méthode **BindToRecordset** de l'interface **IADORecordBinding** lie les champs à des variables C/C++. La méthode **AddNew** ajoute une nouvelle ligne à l'objet **Recordset** lié. La méthode **Update** remplit des champs dans des nouvelles lignes de l'objet **Recordset** ou met à jour des champs de lignes existantes, avec la valeur des variables C/C++.

L'interface **IADORecordBinding** est implémentée par l'objet **Recordset**. Vous n'avez pas à coder l'implémentation vous-même.

## <a name="binding-entries"></a>Entrées de liaison

Les extensions Visual C++ pour ADO mappent les champs d’un objet [Recordset](recordset-object-ado.md) à des variables C/C++. La définition du mappage entre un champ et une variable s’appelle *entrée de liaison*. Les macros fournissent des entrées de liaison pour les données numériques ainsi que les données de longueur fixe et variable. Les entrées de liaison et les variables C/C++ sont déclarées dans une classe dérivée de la classe des extensions Visual C++, **CADORecordBinding**. La classe **CADORecordBinding** est définie en interne par les macros des entrées de liaison.

En interne, ADO mappe les paramètres de ces macros à une structure **DBBINDING** OLE DB et crée un objet **accesseur** OLE DB permettant de gérer le mouvement et la conversion des données entre les champs et les variables. Pour OLE DB, les données se composent de trois parties : une *mémoire tampon* dans laquelle les données sont stockées, un *état* qui indique si un champ a été correctement stocké dans la mémoire tampon ou comment la variable doit être restaurée dans le champ et la *longueur* des données. Pour plus d'informations, consultez le manuel *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data (en anglais).

## <a name="header-file"></a>Fichier d'en-tête

Incluez le fichier suivant dans votre application pour pouvoir utiliser les extensions Visual C++ pour ADO :

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a>Liaison des champs d'un objet Recordset

**Pour lier les champs d'un objet Recordset à des variables C/C++**

1.  Créez une classe dérivée de la classe **CADORecordBinding**.

2.  Spécifiez les entrées de liaison et les variables C/C++ correspondantes dans la classe dérivée. Mettre entre crochets les entrées de liaison entre les macros **BEGIN \_ ADO \_ BINDING** et **END \_ ADO \_ BINDING.** Les macros ne doivent pas se terminer par des virgules ou des points-virgules. Les délimiteurs appropriés sont spécifiés automatiquement par chaque macro. Spécifiez une entrée de liaison pour chaque champ à mapper à une variable C/C++. Utilisez un membre approprié de la famille de macros ENTRÉE LONGUEUR FIXE **ADO, \_ \_ \_** ENTRÉE NUMÉRIQUE **ADO \_ \_** ou **LONGUEUR \_ VARIABLE \_ \_ ADO.**

3.  Dans votre application, créez une instance de la classe dérivée de **CADORecordBinding**. Obtenez l'interface **IADORecordBinding** de l'objet **Recordset**, puis appelez la méthode **BindToRecordset** pour lier les champs de l'objet **Recordset** aux variables C/C++.

Pour plus d’informations, voir [Exemple d’extensions Visual C++](visual-c-extensions-example.md).

## <a name="interface-methods"></a>Méthodes d'interface

L'interface **IADORecordBinding** comporte trois méthodes : **BindToRecordset**, **AddNew** et **Update**. Le seul argument de chaque méthode est un pointeur vers une instance de la classe dérivée de **CADORecordBinding**. En conséquence, les méthodes **AddNew** et **Update** ne peuvent spécifier aucun des paramètres des méthodes ADO du même nom.

**Syntaxe**

La méthode **BindToRecordset** associe les champs d'un objet **Recordset** à des variables C/C++.

`BindToRecordset(CADORecordBinding *binding)` 

La méthode **AddNew** appelle la méthode ADO éponyme, à savoir la méthode [AddNew](addnew-method-ado.md) ADO, pour ajouter une nouvelle ligne à l'objet **Recordset**.

`AddNew(CADORecordBinding *binding)` 

La méthode **Update** appelle la méthode ADO éponyme, à savoir la méthode [Update](update-method-ado.md) ADO, pour mettre à jour l’objet **Recordset**.

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a>Macros d'entrées de liaison

Les macros d'entrées de liaison définissent l'association entre un champ d'un objet **Recordset** et une variable. Des macros de début et de fin délimitent le jeu d'entrées de liaison.

Des familles de macros sont fournies pour les données de longueur fixe, telles que **adDate** ou **adBoolean**, les donnés numériques, telles que **adTinyInt**, **adInteger** ou **adDouble** et les données de longueur variable, telles que **adChar**, **adVarChar** ou **adVarBinary**. Tous les types numériques, à l'exception de **adVarNumeric**, sont également des données de longueur fixe. Chaque famille possède des jeux de paramètres différents, ce qui vous permet d'exclure des informations de liaison superflues.

Pour plus d'informations, consultez le manuel *OLE DB Programmer's Reference*, Appendix A: Data Types (en anglais).

_**Début des entrées de liaison**_

**BEGIN \_ ADO \_ BINDING**(*Class*)

_**Données de longueur fixe**_

**ADO \_ FIXED \_ LENGTH \_ ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)  
**ADO \_ FIXED \_ LENGTH \_ ENTRY2**(*Ordinal, DataType, Buffer, Modify*)

_**Données numériques**_

**ADO \_ NUMERIC \_ ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)  
**ADO \_ NUMERIC \_ ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)

_**Données de longueur variable**_

**ADO \_ ENTRÉE \_ DE LONGUEUR \_ VARIABLE**(*Ordinal, Type de données, Mémoire tampon, Taille, État, Longueur, Modifier*)  
**ADO \_ VARIABLE \_ LENGTH \_ ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)  
**ADO \_ VARIABLE \_ LENGTH \_ ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)  
**ADO \_ VARIABLE \_ LENGTH \_ ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)

_**Entrées de liaison de fin**_

**END \_ LIAISON \_ ADO**()

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parameter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Classe</em></p></td>
<td><p>Classe dans laquelle sont définies les entrées de liaison et les variables C/C++.</p></td>
</tr>
<tr class="even">
<td><p><em>Ordinal</em></p></td>
<td><p>Nombre ordinal, à partir de un, du champ de l'objet <strong>Recordset</strong> correspondant à la variable C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><em>DataType</em></p></td>
<td><p>Type de données ADO équivalent de la variable C/C++ (les types de données valides sont répertoriés à la rubrique <a href="datatypeenum.md">DataTypeEnum</a>). La valeur du champ de l’objet <strong>Recordset</strong> sera convertie dans ce type de données, si nécessaire.</p></td>
</tr>
<tr class="even">
<td><p><em>Buffer</em></p></td>
<td><p>Nom de la variable C/C++ dans laquelle le champ de l'objet <strong>Recordset</strong> va être stocké.</p></td>
</tr>
<tr class="odd">
<td><p><em>Taille</em></p></td>
<td><p>Taille maximale, en octets, du paramètre <em>Mémoire tampon</em>. Si le paramètre <em>Mémoire tampon</em> contient une chaîne de longueur variable, prévoyez de l'espace pour un zéro de fin.</p></td>
</tr>
<tr class="even">
<td><p><em>État</em></p></td>
<td><p>Nom d'une variable qui indique si le contenu du paramètre <em>Mémoire tampon</em> est valide et si la conversion du champ en <em>Type de données</em> s'est correctement déroulée. Les deux valeurs les plus importantes de cette variable sont <strong>adFldOK</strong>, qui indique que la conversion s'est correctement déroulée, et <strong>adFldNull</strong>, qui indique que la valeur du champ est un VARIANT de type VT_NULL et que ce champ n'est pas simplement vide. Les valeurs possibles <em>pour l’état</em> sont répertoriées dans le tableau suivant, &quot; Valeurs d’état.&quot;</p></td>
</tr>
<tr class="odd">
<td><p><em>Modify</em></p></td>
<td><p>Indicateur booléen. S'il a la valeur TRUE, il indique qu'ADO est autorisé à mettre à jour l'objet <strong>Recordset</strong> correspondant avec la valeur contenue dans le paramètre <em>Mémoire tampon</em>.
 Affectez la valeur TRUE au paramètre <em>modifier</em> booléen pour permettre à ADO de mettre à jour le champ lié et la valeur FALSE si vous voulez examiner le champ sans le modifier.</p></td>
</tr>
<tr class="even">
<td><p><em>Précision</em></p></td>
<td><p>Nombre de chiffres pouvant être représenté dans une variable numérique.</p></td>
</tr>
<tr class="odd">
<td><p><em>Scale</em></p></td>
<td><p>Nombre de décimales dans une variable numérique.</p></td>
</tr>
<tr class="even">
<td><p><em>Length</em></p></td>
<td><p>Nom d'une variable à quatre octets qui doit contenir la longueur réelle des données dans <em>Mémoire tampon</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a>Valeurs du paramètre État

La valeur de la variable *État* indique si un champ a été correctement copié dans une variable.

Lorsque vous définissez les données, vous pouvez affecter à *État* la valeur **adFldNull** pour indiquer que le champ de l'objet **Recordset** doit avoir une valeur null.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Une valeur de champ non null a été retournée.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldBadAccessor</strong></p></td>
<td><p>1</p></td>
<td><p>Liaison non valide.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>La valeur n'a pas pu être convertie pour une raison autre qu'une non correspondance de signes ou un dépassement de capacité.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldNull</strong></p></td>
<td><p>3</p></td>
<td><p>Lors de l'obtention d'un champ, indique qu'une valeur null a été retournée. Lors de la définition d'un champ, indique que le champ doit être affecté de la valeur <strong>NULL</strong> lorsqu'il ne peut pas coder lui-même la valeur <strong>NULL</strong> (par exemple, un tableau de caractères ou un nombre entier).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldTruncated</strong></p></td>
<td><p>4 </p></td>
<td><p>Des données de longueur variable ou des chiffres ont été tronqués.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSignMismatch</strong></p></td>
<td><p>5 </p></td>
<td><p>La valeur est signée et le type de données de la variable ne l'est pas.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldDataOverFlow</strong></p></td>
<td><p>6 </p></td>
<td><p>La valeur est supérieure à la capacité de stockage du type de données de la variable.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldCantCreate</strong></p></td>
<td><p>7 </p></td>
<td><p>Type de colonne inconnu et champ déjà ouvert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnavailable</strong></p></td>
<td><p>8 </p></td>
<td><p>La valeur du champ n'a pas pu être déterminée, par exemple, sur un nouveau champ non assigné et ne comportant aucune valeur par défaut.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldPermissionDenied</strong></p></td>
<td><p>9 </p></td>
<td><p>Lors d'une mise à jour, absence d'autorisation d'écriture des données.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Lors d'une mise à jour, la valeur du champ enfreint l'intégrité de la colonne.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Lors d'une mise à jour, la valeur du champ ne respecte pas le schéma de colonne.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldBadStatus</strong></p></td>
<td><p>12 </p></td>
<td><p>Lors d'une mise à jour, paramètre d'état incorrect.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Lors d'une mise à jour, une valeur par défaut a été utilisée.</p></td>
</tr>
</tbody>
</table>

