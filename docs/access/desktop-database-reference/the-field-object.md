---
title: Objet Field (référence de base de données de bureau Access)
TOCTitle: The Field object
ms:assetid: 55531e04-d74f-6394-df64-1660e5d572ca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249284(v=office.15)
ms:contentKeyID: 48544926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2cbd5752399e5a14f08b7eb944e3a028ba53f561
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314020"
---
# <a name="field-object"></a>Field, objet

**S’applique à** : Access 2013, Office 2013

Chaque objet **Field** correspond généralement à une colonne d'une table de base de données. Cependant, un **champ** peut également représenter un pointeur vers un autre **jeu d'enregistrements**, appelé un chapitre. Les exceptions, comme les colonnes de chapitre, seront traitées plus avant dans ce guide.

Utilisez la propriété **Value** des objets **Field** pour définir ou renvoyer des données à l'enregistrement actif. Selon la fonctionnalité du fournisseur, certaines collections, méthodes ou propriétés d'un objet **Field** peuvent ne pas être disponibles.

Avec les collections, méthodes et propriétés d'un objet **Field**, vous pouvez effectuer les opérations suivantes :

- Retourner le nom d'un champ à l'aide de la propriété **Name**.

- Afficher ou modifier les données d'un champ à l'aide de la propriété **Value**. **Value** est la propriété par défaut de l'objet **Field**.

- Retourner les caractéristiques de base d'un champ à l'aide des propriétés **Type**, **Precision** et **NumericScale**.

- Renvoyer la taille déclarée d'un champ à l'aide de la propriété **DefinedSize**.

- Renvoyer la taille réelle des données d'un champ précis à l'aide de la propriété **ActualSize**.

- Déterminer les types de fonctionnalité pris en charge par un champ donné à l'aide de la propriété **Attributes** et de la collection **Properties**.

- Manipuler les valeurs des champs contenant des données binaires longues ou de caractères longs à l'aide des méthodes **AppendChunk** et **GetChunk**.

- Résoudre les incohérences des valeurs de champs au cours d'une mise à jour en lot à l'aide des propriétés **OriginalValue** et **UnderlyingValue**, si le fournisseur prend en charge les mises à jour en lot.

## <a name="describing-a-field"></a>Description d'un champ

Les rubriques suivantes abordent les propriétés de l'objet [Field](field-object-ado.md) qui représentent les informations décrivant l'objet **Field** lui-même  autrement dit, les métadonnées du champ. Ces informations permettent de déterminer une bonne partie du schéma du **jeu d'enregistrements**. Ces propriétés sont **Type**, **DefinedSize**, **ActualSize**, **Name**, **NumericScale** et **Precision**.

## <a name="discovering-the-data-type"></a>Découverte du type de données

La propriété **Type** indique le type de données du champ. Les constantes énumérées de type de données prises en charge par ADO sont décrites dans [DataTypeEnum](datatypeenum.md) dans le *Guide de référence du programmeur ADO*.

Pour les types numériques en virgule flottante comme **adNumeric**, vous pouvez obtenir plus d'informations. La propriété **NumericScale** indique le nombre de chiffres à droite du point décimal utilisé pour représenter les valeurs du **champ**. La propriété **Precision** spécifie le nombre maximal de chiffres utilisé pour représenter les valeurs du **champ**.

## <a name="determining-field-size"></a>Détermination de la taille du champ

Utilisez la propriété **DefinedSize** pour déterminer la capacité de données d'un objet **Field**.

Utilisez la propriété **ActualSize** pour renvoyer la longueur réelle de la valeur d'un objet **Field**. La propriété **ActualSize** est en lecture seule pour tous les champs. Si ADO ne peut pas déterminer la longueur de la valeur de l'objet **Field**, la propriété **ActualSize** renvoie **adUnknown**.

Les propriétés **DefinedSize** et **ActualSize** ont des finalités différentes. Prenez l'exemple d'un objet **Field** avec un type déclaré de **adVarChar** et une valeur de propriété **DefinedSize** de 50 contenant un seul caractère. La valeur de propriété **ActualSize** retournée est la longueur en octets du caractère unique.

## <a name="determining-field-contents"></a>Déterminer le contenu du champ

L'identificateur de la colonne de la source de données est représenté par la propriété **Name** du **champ**. La propriété **Value** de l'objet **Field** renvoie ou définit le contenu de données réel du champ. Il s'agit de la propriété par défaut.

Pour modifier les données d'un champ, attribuez à la propriété **Value** une valeur correspondant au type correct. Votre type de curseur doit prendre en charge les mises à jour pour pouvoir modifier le contenu d'un champ. Dans ce cas précis, la validation de la base de données n'est pas effectué par lot ; il vous faut donc vérifier les erreurs lorsque vous invoquez **UpdateBatch**. Certains fournisseurs prennent également en charge les propriétés **OriginalValue** et **UnderlyingValue** de l'objet **Field** pour vous aider à résoudre les conflits lorsque vous réalisez des mises à jour en lot. Pour en savoir plus sur la résolution de ces conflits, reportez-vous au [chapitre 4 : Modification des données](chapter-4-editing-data.md).

> [!NOTE]
> [!REMARQUE] Vous ne pouvez pas définir les valeurs **Recordset Field** lorsque vous ajoutez de nouveaux **champs** à un **jeu d'enregistrements**. Vous pouvez en revanche ajouter de nouveaux **champs** à un **jeu d'enregistrements** fermé. Vous devez ensuite ouvrir le **jeu d'enregistrements** pour pouvoir affecter des valeurs à ces **champs**.

## <a name="getting-more-field-information"></a>Obtenir des informations de champ supplémentaires

Les objets ADO possèdent deux types de propriétés : intégré et dynamique. À ce stade, seules les propriétés intégrées de l'objet **Field** on été abordées.

Les propriétés intégrées sont les propriétés implémentées dans ADO et immédiatement disponibles pour tout nouvel objet, à l'aide de la syntaxe. Elles n'apparaissent pas comme des objets **Property** dans la collection **Properties** d'un objet.

Les propriétés dynamiques sont définies par le fournisseur de données sous-jacent et apparaissent dans la collection **Properties** de l'objet ADO correspondant. Par exemple, une propriété spécifique au fournisseur peut indiquer si un objet **Recordset** prend en charge les transactions ou les mises à jour. Ces propriétés supplémentaires apparaissent comme des objets **Property** dans la collection **Properties** de cet objet **Recordset**. Les propriétés dynamiques peuvent être référencées uniquement via la collection à l'aide de la syntaxe MyObject. Properties (0) ou de MyObject. Properties ("nom").

Vous ne pouvez supprimer ni l'un ni l'autre de ces deux types de propriétés.

Un objet **Property** dynamique possède quatre propriétés intégrées :

- Sa propriété **Name** est une chaîne qui identifie la propriété.

- Sa propriété **Type** est un entier qui spécifie le type de données de la propriété.

- La propriété **Value** est une variante qui contient le paramètre de la propriété. **Value** est la propriété par défaut d'un objet **Property**.

- La propriété **Attributes** est une valeur **Long** qui indique les caractéristiques de la propriété propre au fournisseur.

La collection **Properties** de l'objet **Field** contient des métadonnées supplémentaires relatives au champ. Le contenu de cette collection varie en fonction du fournisseur. L'exemple de code suivant examine la collection **Properties** de l'exemple de **jeu d'enregistrements** présenté au début de ce chapitre. Il étudie d'abord le contenu de la collection. Ce code utilise le [fournisseur OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md). La collection **Properties** renferme donc les informations propres à ce fournisseur.

```vb 
 
'BeginFieldProps 
 Dim objProp As ADODB.Property 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 
 For Each objProp In objFields(intLoop).Properties 
 Debug.Print vbTab & objProp.Name & " = " & objProp.Value 
 Next objProp 
 Next intLoop 
'EndFieldProps 
```

## <a name="dealing-with-binary-data"></a>Traitement des données binaires

Utilisez la méthode [AppendChunk](appendchunk-method-ado.md) sur un objet **Field** pour le remplir de données binaires longues ou de caractères longs. Si vous manquez de mémoire système, vous pouvez utiliser la méthode **AppendChunk** pour manipuler une partie des valeurs longues plutôt que leur totalité.

Si la section **adFldLong** de la propriété **Attributes** d'un objet **Field** est définie sur **True**, vous pouvez utiliser la méthode **AppendChunk** pour ce champ.

La première invocation de la méthode **AppendChunk** sur un objet **Field** écrit les données dans le champ en écrasant toute donnée existante. Les invocations suivantes de **AppendChunk** s'ajoutent aux données existantes. Si vous ajoutez des données à un champ, puis définissez ou lisez la valeur d'un autre champ de l'enregistrement actif, ADO suppose que vous avez terminé l'ajout de données dans le premier champ. Si vous invoquez à nouveau la méthode **AppendChunk** sur le premier champ, ADO interprète l'invocation comme une nouvelle opération **AppendChunk** et écrase les données existantes. L'accès à des champs d'autres objets **Recordset** non identiques au premier objet **Recordset** n'interrompt pas les opérations **AppendChunk**.

Utilisez la méthode **GetChunk** sur un objet **Field** pour en extraire toute ou partie des données binaires ou de caractères longues. Si vous manquez de mémoire système, vous pouvez utiliser la méthode **GetChunk** pour manipuler une partie des valeurs longues plutôt que leur totalité.

Les données qu'un appel à la méthode **GetChunk** retourne sont assignées à une *variable*. Si *Taille* est supérieur aux données restantes, la méthode  **GetChunk ** retourne uniquement les données restantes sans remplir la *variable* avec des espaces vides. Si le champ est vide, la méthode **GetChunk** renvoie une valeur NULL.

Chaque invocation **GetChunk** suivante reprend l'extraction des données à l'endroit où l'invocation **GetChunk** précédente s'est arrêtée. Cependant, si vous extrayez des données d'un champ et que vous définissez ou lisez ensuite la valeur d'un autre champ de l'enregistrement actif, ADO suppose que vous avez terminé l'extraction des données du premier champ. Si vous invoquez à nouveau la méthode **GetChunk** sur le premier champ, ADO interprète l'invocation comme une nouvelle opération **GetChunk** et commence la lecture des données du début. L'accès aux champ d'autres objets **Recordset** non identiques au premier objet **Recordset** n'interrompt pas les opérations **GetChunk**.

Si la section **adFldLong** de la propriété **Attributes** d'un objet **Field** est définie sur **True**, vous pouvez utiliser la méthode **GetChunk** sur ce champ.

S'il n'existe aucun enregistrement actif lorsque vous utilisez la méthode **GetChunk** ou **AppendChunk** sur un objet **Field**, l'erreur 3021 (aucun enregistrement actif) survient.

Pour un exemple d'utilisation de ces méthodes pour manipuler des données binaires, reportez-vous aux exemples de méthodes [AppendChunk](appendchunk-method-ado.md) et [GetChunk](getchunk-method-ado.md) dans le *Guide de référence du programmeur ADO*.

