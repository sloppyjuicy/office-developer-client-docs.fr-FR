---
title: Recordset, objet (ADO)
TOCTitle: Recordset object (ADO)
ms:assetid: 0f963bf8-f066-dc8a-b754-f427de712df1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248865(v=office.15)
ms:contentKeyID: 48543267
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 636681cf8e0c20f078387b21974141a9cb66cfcd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719994"
---
# <a name="recordset-object-ado"></a>Recordset, objet (ADO)

**S’applique à**: Access 2013, Office 2013

Représente le jeu entier d'enregistrements d'une table de base ou les résultats d'une commande exécutée. L'objet **Recordset** ne peut faire référence qu'à un seul enregistrement à l'intérieur du jeu en tant qu'enregistrement actif.

## <a name="remarks"></a>Notes

Les objets **Recordset** servent à manipuler les données provenant d'un fournisseur. Lorsque vous utilisez ADO, vous manipulez des données presqu'exclusivement à l'aide d'objets **Recordset**. Tous les objets **Recordset** sont constitués d'enregistrements (lignes) et de champs (colonnes). Selon les fonctionnalités prises en charge par le fournisseur, certaines méthodes ou propriétés de **Recordset** risquent de ne pas être disponibles.

ADODB.Recordset est l'identificateur de programme (ProgID) qui doit être utilisé pour créer un objet **Recordset**. Les applications existantes qui font référence aux ProgID ADOR.Recordset obsolètes continueront à fonctionner sans être recompilées, mais les nouvelles applications développées doivent faire référence à ADODB.Recordset.

Il existe quatre types de curseurs définis dans ADO :

  - **Curseur dynamique**  Permet de visualiser des ajouts, des modifications et des suppressions effectués par d'autres utilisateurs ; permet d'effectuer tous types de déplacements dans l'objet **Recordset** qui ne repose pas sur les signets ; prend également l'utilisation de signets si le fournisseur les prend en charge.

  - **Curseur de jeu de clés**  Se comporte comme un curseur dynamique, sauf qu'il empêche l'affichage des enregistrements ajoutés par d'autres utilisateurs et l'accès aux enregistrements supprimés par ceux-ci. Les modifications apportées aux données par d'autres utilisateurs restent visibles. Ce curseur prend en charge les signets et permet donc tous types de déplacements à l'intérieur du **Recordset**.

  - **Curseur statique**  Fournit une copie statique d'un jeu d'enregistrements pour que vous puissiez y rechercher des données ou générer des rapports ; permet l'utilisation de signets et donc tous types de déplacements à l'intérieur du **Recordset**. Les ajouts, modifications et suppressions effectués par les autres utilisateurs ne sont pas visibles. Il s'agit du seul type de curseur accepté lorsque vous ouvrez un objet **Recordset** côté client.

  - **Curseur en avance seule**  Permet uniquement le défilement en avant à l'intérieur du **Recordset**. Les ajouts, modifications et suppressions effectués par les autres utilisateurs ne sont pas visibles. Cela permet d'améliorer les performances lorsque vous ne devez effectuer qu'un seul passage dans un objet **Recordset**.

Définissez la propriété [CursorType](cursortype-property-ado.md) avant l’ouverture de l' **objet Recordset** pour choisir le type de curseur, ou passez un argument *CursorType* avec la méthode [Open](open-method-ado-recordset.md) . Certains fournisseurs ne prennent pas en charge tous les types de curseur. Consultez la documentation spécifique du fournisseur. Si vous ne spécifiez pas de type de curseur, ADO ouvre un curseur en avance seule par défaut.

Si la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient** pour ouvrir un **Recordset**, la propriété **UnderlyingValue** sur les objets [Field](field-object-ado.md) n'est pas disponible dans l'objet **Recordset** renvoyé. S'ils sont utilisés avec certains fournisseurs (comme Microsoft ODBC Provider for OLE DB conjointement avec Microsoft SQL Server), vous pouvez créer des objets **Recordset** indépendamment d'un objet [Connection](connection-object-ado.md) déjà défini, en transmettant une chaîne de connexion avec la méthode **Open**. ADO crée tout de même un objet [Connection](connection-object-ado.md), il ne l'affecte pas à une variable objet. Toutefois, si vous ouvrez plusieurs objets **Recordset** sur la même connexion, il est conseillé de créer un objet **Connection** de manière explicite et de l'ouvrir ; l'objet **Connection** est ainsi affecté à une variable objet. Si vous n'utilisez pas de variable objet lorsque vous ouvrez vos objets **Recordset**, ADO crée un nouvel objet **Connection** pour chaque nouveau **Recordset**, même si vous transmettez la même chaîne de connexion.

Vous pouvez créer autant d'objets **Recordset** que nécessaire.

Lorsque vous ouvrez un **Recordset**, l'enregistrement actif est le premier enregistrement (s'il existe) et les propriétés [BOF](bof-eof-properties-ado.md) et [EOF](bof-eof-properties-ado.md) prennent la valeur **False**. S'il n'existe pas d'enregistrement, les paramètres de la propriété **BOF** et **EOF** ont la valeur **True**.

Vous pouvez utiliser les méthodes [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), **MoveLast**, **MoveNext** et **MovePrevious**, la méthode [Move](move-method-ado.md) ainsi que les propriétés [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) et [Filter](filter-property-ado.md) pour repositionner l’enregistrement actif, à condition que le fournisseur prenne en charge la fonctionnalité requise. Les objets **Recordset** ne prennent en charge que la méthode [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md). Si vous utilisez les méthodes **Move** pour consulter chaque enregistrement (ou énumérer l’objet **Recordset**), vous pouvez utiliser les propriétés **BOF** et **EOF** pour déterminer si vous vous avez dépassé le début ou la fin de l’objet **Recordset**.

Les objets **Recordset** peuvent prendre en charge deux types de mise à jour : immédiate et par lot. Avec la mise à jour immédiate, toutes les modifications apportées aux données sont écrites instantanément dans la source de données sous-jacente lorsque vous appelez la méthode [Update](update-method-ado.md). Vous pouvez également passer des tableaux de valeurs comme paramètres avec les méthodes [AddNew](addnew-method-ado.md) et **Update** et mettre à jour plusieurs champs simultanément dans un enregistrement.

Si un fournisseur prend en charge la mise à jour par lot, vous pouvez décider que le fournisseur mette en cache plusieurs enregistrements et les transmette ensuite par l'intermédiaire d'un seul appel à la base de données ; utilisez pour cela la méthode [UpdateBatch](updatebatch-method-ado.md). Cela s'applique aux modifications effectuées avec les méthodes **AddNew**, **Update** et [Delete](delete-method-ado-recordset.md). Après avoir appelé la méthode **UpdateBatch**, vous pouvez recourir à la propriété [Status](status-property-ado-recordset.md) pour rechercher les éventuels conflits au niveau des données afin de les résoudre.

> [!NOTE]
> [!REMARQUE] Pour exécuter une requête sans utiliser d'objet [Command](command-object-ado.md), passez une chaîne de requête à la méthode **Open** d'un objet **Recordset**. Toutefois, un objet **Command** est nécessaire si vous voulez rendre persistant le texte de commande et l'exécuter de nouveau, ou utiliser des paramètres de requête.

La propriété [Mode](mode-property-ado.md) régit les autorisations d'accès.

La collection **Fields** est le membre par défaut de l'objet **Recordset**. Les deux instructions suivantes sont donc équivalentes.

```vb
    Debug.Print objRs.Fields.Item(0)  ' Both statements print 
    Debug.Print objRs(0)              '  the Value of Item(0).
```
