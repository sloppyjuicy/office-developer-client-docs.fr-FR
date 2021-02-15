---
title: Programmation ADO Visual C++
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a890b4906fb9f207f12ff17ef0d3ccf1a97a44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302771"
---
# <a name="visual-c-ado-programming"></a>Programmation ADO Visual C++

**S’applique à** : Access 2013, Office 2013

La documentation Référence de l'API ADO décrit les fonctionnalités de l'interface de programmation d'application (API) ADO en employant une syntaxe similaire à celle de Microsoft Visual Basic. Bien que le public visé soit tous les utilisateurs, les programmeurs ADO utilisent divers langages tels que Visual Basic, Visual C++ (avec et sans **la \#** directive d’importation) et Visual J++ (avec le package de classeS ADO/WFC).

Pour répondre à cette diversité, les [index de la syntaxe ADO pour Visual C++](using-ado-with-microsoft-visual-c.md) proposent une syntaxe spécifique au langage Visual C++ avec des liens vers des descriptions communes de fonctionnalités, paramètres, comportements exceptionnels, etc. de la documentation Référence de l'API ADO.

ADO est implémenté avec les interfaces COM (Component Object Model). Toutefois, pour les programmeurs, il est plus facile d'utiliser COM avec certains langages de programmation qu'avec d'autres. Par exemple, presque tous les détails liés à l'utilisation de COM sont gérés implicitement pour les programmeurs qui ont recours à Visual Basic, tandis que les programmeurs Visual C++ doivent gérer eux-mêmes ces détails.

Les sections suivantes résument les détails pour les programmeurs C et C++ qui utilisent ADO et la directive **\# d’importation.** Il se concentre sur les types de données spécifiques à COM (**Variant,** **BSTR** et **SafeArray**) et la gestion des erreurs \_ (erreur \_ com).

## <a name="using-the-import-compiler-directive"></a>Utilisation de la \# directive du compilateur d’importation

La directive **\# import** du compilateur Visual C++ simplifie l’travail avec les méthodes et propriétés ADO. La directive extrait le nom d'un fichier contenant une bibliothèque de types, telle que le fichier .dll ADO (Msado15.dll), et génère des fichiers d'en-tête contenant des déclarations typedef, des pointeurs intelligents pour les interfaces, ainsi que des constantes énumérées. Chaque interface est encapsulée dans une classe.

Pour chaque opération qui se produit à l'intérieur d'une classe (c'est-à-dire, un appel de méthode ou de propriété), il existe une déclaration permettant d'appeler directement l'opération (c'est-à-dire, la forme « brute » de l'opération), et une déclaration qui appelle l'opération brute et lève une exception COM si l'opération ne s'exécute pas correctement. Si l'opération est une propriété, il existe généralement une directive de compilateur qui crée une autre syntaxe si l'opération présente une syntaxe apparentée à Visual Basic.

Les opérations qui récupèrent la valeur d’une propriété ont des noms de formulaire, **Get***Property*. Les opérations qui définissent la valeur d’une propriété ont des noms de forme, **Put***Property*. Les opérations qui définissent la valeur d’une propriété avec un pointeur vers un objet ADO ont des noms de formulaire, **PutRef***, propriété*.

Vous pouvez obtenir ou définir une propriété avec des appels se présentant comme suit :

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Utilisation des directives de propriété

La directive de compilateur **\_ \_ declspec(property...)** est une extension de langage C spécifique à Microsoft qui déclare une fonction utilisée comme propriété pour avoir une syntaxe alternative. Par conséquent, vous pouvez définir ou obtenir les valeurs d'une propriété d'une façon similaire à Visual Basic. Par exemple, vous pouvez définir et obtenir une propriété comme suit :

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Notez qu'il n'est pas utile de coder les éléments suivants :

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

Le compilateur génère l’appel de propriété **Get***-*, **Put**-, ou **PutRef***,* en fonction de la syntaxe alternative déclarée et selon que la propriété est en cours de lecture ou d’écriture.

La directive du compilateur **\_ \_ declspec(property...)** peut uniquement  déclarer **obtenir,** placer ou **obtenir** et placer une syntaxe alternative pour une fonction.  Les opérations en lecture seule ne peuvent avoir qu'une déclaration **get** et les opérations en écriture seule une déclaration **put**; les opérations en lecture et en écriture ont à la fois des déclarations **get** et **put**.

Seules deux déclarations sont possibles avec cette directive ; toutefois, chaque propriété peut avoir trois fonctions de propriété : **Get***Property*, **Put***Property* et **PutRef**Property*. Dans ce cas, deux formes seulement de la propriété possèdent une syntaxe alternative.

Par exemple, la propriété **ActiveConnection de** l’objet **Command** est déclarée avec une syntaxe alternative pour **Get***ActiveConnection* et **PutRef***ActiveConnection*. La syntaxe **PutRef**- s'avère un bon choix car, dans la pratique, il est courant de spécifier un objet **Connection** ouvert (c'est-à-dire, un pointeur d'objet **Connection**) dans cette propriété. En revanche, l’objet **Recordset** possède des opérations **Get**-, **Put**-, et **PutRef***ActiveConnection,* mais aucune syntaxe alternative.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Collections, méthode GetItem et propriété Item

ADO définit plusieurs collections, notamment **Fields**, **Parameters**, **Properties** et **Errors**. En Visual C++, la **méthode GetItem(***index***)** renvoie un membre de la collection. *Index* est une valeur de type **Variant**, qui représente soit un index numérique du membre de la collection, soit une chaîne contenant le nom du membre.

La directive du compilateur **\_ \_ declspec(property...)** déclare la propriété **Item** en tant que syntaxe alternative à la méthode **GetItem()** fondamentale de chaque collection. La syntaxe alternative utilise des crochets droits et présente des similitudes avec une référence de matrice. En règle générale, les deux formes se présentent comme suit:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Par exemple, attribuez une valeur à un champ d'un objet **Recordset**, nommé ***rs***, dérivé de la table **authors** de la base de données **pubs**. Utilisez la **propriété Item()**  pour accéder au troisième champ de la collection **Fields** de l’objet **Recordset** (les collections sont indexées à partir de zéro ; supposons que le troisième champ est nommé ***au \_ fname***). Appelez ensuite la méthode **Value()** sur l'objet **Field** pour attribuer une valeur de chaîne.

Ceci peut être exprimé en Visual Basic avec les quatre variantes suivantes (les deux dernières sont propres à Visual Basic ; les autres langages n'ont pas d'équivalents) :

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

En Visual C++, l'équivalent des deux premières variantes est :

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

\-or- (la syntaxe alternative de la **propriété Value** est également affichée)

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>Types de données propres à COM

En règle générale, les types de données Visual Basic que vous rencontrez dans la documentation Référence de l'API ADO possèdent un équivalent Visual C++. Il peut s'agir notamment des types de données standard **unsigned char** pour **Byte** en Visual Basic, **short** pour **Integer** et **long** pour **Long**. Consultez les index de la syntaxe pour savoir exactement quelles sont les exigences au niveau des opérandes d'une méthode ou d'une propriété donnée.

Les exceptions à cette règle sont les types de données spécifiques à COM : **Variant**, **BSTR** et **SafeArray**.

### <a name="variant"></a>Variant

A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.

La **\_ classe variant \_ t** encapsule et gère le type de données **Variant.**

Lorsque la référence de l’API ADO indique qu’un opérande de méthode ou de propriété prend une valeur, cela signifie généralement que la valeur est passée dans une **\_ variante \_ t**.

Cette règle est explicitement vraie lorsque la section **Parameters** des rubriques de la documentation Référence de l'API ADO indique qu'un opérande est de type **Variant**. Des exceptions sont possibles, notamment lorsque la documentation précise explicitement que l'opérande correspond à un type de données standard, tel que **Long** ou **Byte**, ou encore lorsque l'opérande correspond à un type de données **String**.

### <a name="bstr"></a>BSTR

**BSTR** (**B** asic **STR** ing) est un type de données structuré qui contient une chaîne de caractères ainsi que la longueur de celle-ci. COM fournit des méthodes permettant d'allouer, manipuler et libérer un type **BSTR**.

La **\_ classe bstr \_ t** encapsule et gère le type de données **BSTR.**

Lorsque la référence de l’API ADO indique qu’une méthode ou une propriété prend une valeur **string,** cela signifie que la valeur est sous la forme d’un **\_ bstr \_ t**.

#### <a name="casting-_variant_t-and-_bstr_t-classes"></a>Casting \_ des \_ classes variant t \_ et bstr \_ t

Souvent, il n’est pas nécessaire de coder explicitement une **\_ variante \_ t** ou **\_ bstr \_ t** dans un argument d’une opération. Si la classe **\_ variant \_ t** ou **\_ bstr \_ t** possède un constructeur qui correspond au type de données de l’argument, le compilateur génère la variante **\_ \_ t** ou **\_ bstr \_ t appropriée.**

Toutefois, si l'argument est ambigu, c'est-à-dire si le type de données de l'argument correspond à plusieurs constructeurs, vous devez attribuer à l'argument le type de données approprié pour appeler le constructeur correct.

Par exemple, la déclaration pour la méthode **Recordset::Open** est :

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

L’argument ActiveConnection prend une référence à une variante **\_ \_ t**, que vous pouvez coder en tant que chaîne de connexion ou pointeur vers un objet **Connection** ouvert.

La variante **\_ \_ t** correcte sera construite implicitement si vous passez une chaîne telle que « DSN=pubs;uid=sa;pwd=; » ou un pointeur tel que « (IDispatch \* ) pConn ».

Vous pouvez également coder explicitement une variante **\_ \_ t** contenant un pointeur tel que « \_ variant \_ t((IDispatch \* ) pConn, true) ». Le cast, (IDispatch ), résout l’ambiguïté avec un autre constructeur qui prend un pointeur vers une \* interface IUnknown.

Bien qu'il s'agisse d'un fait rarement mentionné, il est essentiel de rappeler qu'ADO est une interface IDispatch. Chaque fois qu'un pointeur d'objet ADO doit être passé en tant que **Variant**, ce pointeur doit être converti en pointeur vers une interface IDispatch.

Dans le dernier cas, le deuxième argument booléen du constructeur est explicitement codé avec sa valeur facultative par défaut, true. Cet argument entraîne l’appel de la méthode **AddRef**() par le constructeur **Variant,** ce qui permet à ADO d’appeler automatiquement la méthode **\_ \_ variant t::Release**() une fois l’appel de la méthode ou de la propriété ADO terminé.

### <a name="safearray"></a>SafeArray

**SafeArray** est un type de données structuré qui contient un tableau d'autres types de données. **SafeArray** est considéré comme étant sûr (*safe* en anglais) car ce type de données contient des informations sur les limites de chaque dimension du tableau, et il restreint l'accès aux éléments du tableau qui se trouvent à l'intérieur de ces limites.

Lorsque la documentation Référence de l'API ADO indique qu'une méthode ou une propriété prend ou retourne un tableau, cela signifie que la méthode ou la propriété prend ou retourne un type **SafeArray**, et non un tableau C/C++ natif.

For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values. Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**. It is that other **Variant** that is passed as the second argument of **OpenSchema**.

Pour prendre d'autres exemples, le premier argument de la méthode **Find** est un **Variant** dont la valeur est un tableau **SafeArray** unidimensionnel ; chacun des deux premiers arguments facultatifs de **AddNew** est un tableau **SafeArray** unidimensionnel ; et la valeur retournée par la méthode **GetRows** est un type **Variant** dont la valeur est un tableau **SafeArray** à deux dimensions.

## <a name="missing-and-default-parameters"></a>Paramètres manquants et par défaut

Visual Basic autorise les paramètres manquants au niveau des méthodes. Par exemple, la méthode **Open** de l'objet **Recordset** présente cinq paramètres. Or, vous pouvez ignorer les paramètres intermédiaires et omettre les paramètres finaux. Ainsi, une valeur **BSTR** ou **Variant** par défaut leur sera substituée en fonction du type de données de l'opérande manquant.

Dans le cas de C/C++, tous les opérandes doivent être spécifiés. Si vous souhaitez spécifier un paramètre manquant dont le type de données est une chaîne, spécifiez un **\_ bstr \_ t** contenant une chaîne null. Si vous souhaitez spécifier un paramètre manquant dont le type de données est **variant,** spécifiez une variante **\_ \_ t** avec une valeur DISP \_ E PARAMNOTFOUND et un type d’erreur \_ \_ VT. Vous pouvez également spécifier la constante **\_ de variante \_ t** équivalente, **vtMissing,** fournie par la directive **\# d’importation.**

Il existe trois méthodes qui constituent des exceptions à l'utilisation habituelle de **vtMissing**. Il s'agit des méthodes **Execute** des objets **Connection** et **Command**, et de la méthode **NextRecordset** de l'objet **Recordset**. Voici leurs signatures :

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Les paramètres  *RecordsAffected* et *Parameters* sont des pointeurs vers un **Variant**.  *Parameters* est un paramètre d'entrée qui spécifie l'adresse d'un **Variant** contenant un paramètre unique, ou un tableau de paramètres, qui modifiera la commande exécutée.  *RecordsAffected* est un paramètre de sortie qui spécifie l'adresse d'un **Variant** lorsque le nombre de lignes affectées par la méthode est retourné.

Dans la méthode **Execute** de l’objet **Command,** indiquez qu’aucun paramètre n’est spécifié en paramétant *Parameters* sur vtMissing (ce qui est recommandé) ou sur le \& pointeur null (autrement dit, **NULL** ou zéro (0)). Si *Parameters* est associé au pointeur Null, la méthode remplace en interne l'équivalent de **vtMissing**, puis termine l'opération.

Dans toutes les méthodes, vous pouvez indiquer que le nombre d'enregistrements affectés ne doit pas être retourné en associant *RecordsAffected* au pointeur Null. Dans ce cas, le pointeur Null ne représente pas réellement le paramètre manquant mais indique plutôt que la méthode doit ignorer le nombre d'enregistrements affectés.

Par conséquent, pour ces trois méthodes, le code suivant est approprié :

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Gestion des erreurs

Dans COM, la plupart des opérations renvoient un code de retour HRESULT qui indique si une fonction a été correctement exécutée. La directive **\# d’importation** génère du code de wrapper autour de chaque méthode ou propriété « brute » et vérifie le HRESULT renvoyé. Si HRESULT indique un échec, le code wrapper envoie une erreur COM en appelant \_ com \_ issue errorex() avec le code de retour \_ HRESULT comme argument. Les objets d'erreur COM peuvent être interceptés dans un bloc **try**-**catch**. (Pour plus d’efficacité, capturez une référence à un **\_ objet \_ d’erreur com.)**

Rappelez-vous qu'il s'agit d'erreurs ADO : elles sont le résultat de l'échec d'une opération ADO. Les erreurs retournées par le fournisseur sous-jacent apparaissent en tant qu'objets **Error** dans la collection **Errors** de l'objet **Connection**.

La directive **\# d’importation** crée uniquement des routines de gestion des erreurs pour les méthodes et propriétés déclarées dans le .dll ADO. Toutefois, vous pouvez tirer parti de ce même mécanisme de gestion des erreurs en écrivant votre propre fonction inline ou macro de détection d'erreurs. Vous trouverez des exemples dans la rubrique [Extensions Visual C++ pour ADO](visual-c-extensions-for-ado.md), ou le code présenté dans les sections suivantes.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Équivalents Visual C++ des conventions Visual Basic de la conférence

Vous trouverez ci-dessous un récapitulatif de plusieurs conventions décrites dans la documentation ADO, codées en Visual Basic, ainsi que leurs équivalents en Visual C++.

### <a name="declaring-an-ado-object"></a>Déclaration d’un objet ADO

En langage Visual Basic, une variable d'objet ADO (en l'occurrence, un objet **Recordset** ) est déclarée comme suit :

```vb 
 
Dim rst As ADODB.Recordset 
```

La clause « ADODB. Recordset » est le ProgID de l’objet **Recordset** tel que défini dans le Registre. Une nouvelle instance d'un objet **Record** est déclarée comme suit :

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-or-

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

En Visual C++, la directive **\# d’importation** génère des déclarations de type pointeur intelligent pour tous les objets ADO. Par exemple, une variable qui pointe vers un objet **\_ Recordset** est de type **\_ RecordsetPtr** et est déclarée comme suit :

```cpp 
 
_RecordsetPtr rs; 
```

Une variable qui pointe vers une nouvelle instance d’un objet **\_ Recordset** est déclarée comme suit :

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-or-

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-or-

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

Une fois que la méthode **CreateInstance** a été appelée, la variable peut être utilisée comme suit :

```cpp 
 
rs->Open(...); 
```

Notez que dans un cas, l’opérateur « . » est utilisé comme si la variable était une instance d’une classe (rs. CreateInstance), et dans un autre cas, l’opérateur « - » est utilisé comme si la variable était un pointeur vers une \> interface (rs- \> Open).

Une variable peut être utilisée de deux manières, car l’opérateur « - » est surchargé pour permettre à une instance d’une classe de se comporter comme un pointeur vers \> une interface. Un membre de classe privé de la variable d’instance contient un pointeur vers l’interface **\_ recordset** ; l’opérateur « - » renvoie ce pointeur ; et le pointeur renvoyé accède aux membres de l’objet \> **\_ Recordset.**

### <a name="coding-a-missing-parameter"></a>Codage d’un paramètre manquant

#### <a name="string"></a>String

Lorsque vous devez coder un opérande **String** manquant en Visual Basic, il vous suffit de l'omettre. En Visual C++, vous devez spécifier l'opérande. Codez **\_ un bstr \_ t** qui a une chaîne vide en tant que valeur.

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>Variant

Lorsque vous devez coder un opérande **Variant** manquant en Visual Basic, il vous suffit de l'omettre. En Visual C++, vous devez spécifier tous les opérandes. Codez un paramètre **Variant** manquant avec une **\_ variante \_ t** définie sur la valeur spéciale DISP \_ E \_ PARAMNOTFOUND et le type, VT \_ ERROR. Vous pouvez également **spécifier vtMissing**, qui est une constante prédéfini équivalente fournie par la directive **\# d’importation.**

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-ou utiliser -

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>Déclaration d’une variante

En Visual Basic, un **Variant** est déclaré avec l'instruction **Dim** comme suit :

```vb 
 
Dim VariableName As Variant 
```

En Visual C++, déclarez une variable en tant que variante de type **\_ \_ t**. Quelques déclarations de **\_ \_ variantes t** schématiques sont indiquées ci-dessous.

> [!NOTE]
> [!REMARQUE] Ces déclarations donnent simplement une idée globale du codage que vous effectueriez dans votre propre programme. Pour plus d'informations, consultez les exemples ci-dessous, ainsi que la documentation Visual C++.

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a>Utilisation de tableaux de variantes

En langage Visual Basic, les tableaux de valeurs **Variant** peuvent être codés à l'aide de l'instruction **Dim**. Vous pouvez également utiliser la fonction **Array**, comme illustré dans l'exemple de code suivant :

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

L’exemple Visual C++ suivant illustre l’utilisation **d’un safeArray** utilisé avec une **\_ variante \_ t**.

> [!NOTE]
> [!REMARQUE] Les remarques suivantes correspondent aux sections commentées dans l'exemple de code.

1. À nouveau, la fonction inline TESTHR() est définie pour tirer parti d'un mécanisme de gestion des erreurs existant.

2. Vous avez seulement besoin d'un tableau unidimensionnel pour pouvoir utiliser **SafeArrayCreateVector** à la place de la déclaration **SAFEARRAYBOUND** et de la fonction **SafeArrayCreate** à usage général. Voici comment se présenterait le code si vous utilisiez **SafeArrayCreate**:
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. Le schéma identifié par la constante répertoriée, **adSchemaColumns**, est associé à quatre colonnes de contrainte : TABLE \_ CATALOG, TABLE \_ SCHEMA, TABLE NAME et \_ COLUMN \_ NAME. Par conséquent, un tableau de valeurs **Variant** avec quatre éléments est créé. Ensuite, une valeur de contrainte qui correspond à la troisième colonne, TABLE \_ NAME, est spécifiée. Le **jeu d’enregistrements** renvoyé se compose de plusieurs colonnes, dont un sous-ensemble est constitué des colonnes de contrainte. Les valeurs des colonnes de contrainte pour chaque ligne renvoyée doivent être identiques aux valeurs de contrainte correspondantes.

4. Ceux qui **connaissent SafeArrays** peuvent être surpris que **SafeArrayDestroy**() ne soit pas appelé avant la sortie. En fait, l’appel **de SafeArrayDestroy**() dans ce cas entraîne une exception d’run-time. La raison est que le destructeur pour vtCriteria appelle **VariantClear**() lorsque la **\_ variante \_ t** sort de la portée, ce qui libère **l’array sécurisé**. **L’appel de SafeArrayDestroy,** sans effacer manuellement la **\_ variante \_ t,** aurait pour effet que le destructeur essaierait d’effacer un pointeur **SafeArray** non valide. Si **SafeArrayDestroy a** été appelé, le code se ressemblerait à ceci :
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   Toutefois, il est beaucoup plus simple de laisser la **\_ variante ne \_ pas** gérer **safeArray**.


```cpp 
 
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
    
    // Note 1 
    inline void TESTHR( HRESULT _hr ) 
    { if FAILED(_hr) _com_issue_error(_hr); } 
    
    void main(void) 
    { 
    CoInitialize(NULL); 
    try 
    { 
    _RecordsetPtr pRs("ADODB.Recordset"); 
    _ConnectionPtr pCn("ADODB.Connection"); 
    _variant_t vtTableName("authors"), 
    vtCriteria; 
    long ix[1]; 
    SAFEARRAY *pSa = NULL; 
    
    pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
    adConnectUnspecified); 
    // Note 2, Note 3 
    pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
    if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
    
    // Specify TABLE_NAME in the third array element (index of 2). 
    
    ix[0] = 2; 
    TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
    
    // There is no Variant constructor for a SafeArray, so manually set the 
    // type (SafeArray of Variant) and value (pointer to a SafeArray). 
    
    vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
    vtCriteria.parray = pSa; 
    
    pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
    
    long limit = pRs->GetFields()->Count; 
    for (long x = 0; x < limit; x++) 
    printf("%d: %s\n", x+1, 
    ((char*) pRs->GetFields()->Item[x]->Name)); 
    // Note 4 
    pRs->Close(); 
    pCn->Close(); 
    } 
    catch (_com_error &e) 
    { 
    printf("Error:\n"); 
    printf("Code = %08lx\n", e.Error()); 
    printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
    printf("Source = %s\n", (char*) e.Source()); 
    printf("Description = %s\n", (char*) e.Description()); 
    } 
    CoUninitialize(); 
    } 
```

### <a name="using-property-getputputref"></a>Utilisation de la propriété Get/Put/PutRef

En langage Visual Basic, le fait que le nom d'une propriété soit récupéré, attribué ou qu'une référence lui soit attribuée ne suffit pas à le qualifier.

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

Cet exemple Visual C++ illustre **la propriété Get** / **Put** /* *PutRef***.*

> [!NOTE]
> [!REMARQUE] Les remarques suivantes correspondent aux sections commentées dans l'exemple de code.

1. Cet exemple utilise deux formes d’un argument de chaîne manquant : une constante explicite, **strMissing** et une chaîne que le compilateur utilisera pour créer un **\_ bstr \_ t** temporaire qui existera pour l’étendue de la méthode **Open.**

2. Il n’est pas nécessaire de caster l’opérande de rs- \> PutRefActiveConnection(cn) vers (IDispatch ), car le type de l’opérande est déjà \* (IDispatch \* ).
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="using-getitemx-and-itemx"></a>Utilisation de GetItem(x) et d’élément \[ x\]

Cet exemple Visual Basic illustre la syntaxe standard et alternative de **Item**().

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

Cet exemple Visual C++ illustre **Item**.

> [!NOTE]
> [!REMARQUE] La remarque suivante correspond aux sections commentées dans l'exemple de code.

1. Lorsque l'accès à la collection s'effectue avec **Item**, l'index **2** doit être casté en **long** pour permettre l'appel d'un constructeur approprié.
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="casting-ado-object-pointers-with-idispatch-"></a>Conversion de pointeurs d'objet ADO à l'aide de (IDispatch \*)

L'exemple Visual C++ suivant illustre l'utilisation de (IDispatch \*) pour effectuer un cast des pointeurs d'objet ADO.

> [!NOTE]
> [!REMARQUE] Les remarques suivantes correspondent aux sections commentées dans l'exemple de code.

1. Spécifiez un objet **Connection** ouvert dans un **Variant** explicitement codé. Castez-le avec (IDispatch ) afin \* que le constructeur correct soit appelé. Définissez également explicitement le deuxième paramètre de variante **\_ \_ t** sur la valeur par défaut true **,** afin que le nombre de références d’objets soit correct à la fin de l’opération **Recordset::Open.**

2. L’expression( bstr t) n’est pas un cast, mais un opérateur de variante t qui extrait une chaîne \_ \_ **\_ bstr \_ t** **\_ \_**  à partir de la variante renvoyée par **Value**. L’expression ( char ) n’est pas un cast, mais un opérateur \* **\_ bstr \_ t** qui extrait un pointeur vers la chaîne encapsulée dans un objet **\_ bstr \_ t.** Cette section de code illustre certains des comportements utiles des opérateurs **\_ de variante \_ t** et **\_ bstr \_ t.**
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
   ```

