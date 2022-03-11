---
title: Accès aux fichiers DLL dans Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- accès aux fichiers dlls [Excel 2007], DLLs [Excel 2007], accès dans Excel
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
ms.localizationpriority: high
ms.openlocfilehash: b624f61228def5b61f4efcdf9d6aee2d2eecd63d
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405043"
---
# <a name="access-dlls-in-excel"></a>Accès aux fichiers DLL dans Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Vous pouvez accéder à une commande ou à une fonction DLL dans Microsoft Excel de plusieurs manières :
  
- avec un module de code Microsoft�Visual�Basic pour Applications (VBA) dans lequel la fonction ou commande a �t� rendue disponible � l�aide d�une instruction **Declare**�;

- avec une feuille macro XLM � l�aide des fonctions **CALL** ou **REGISTER**�;

- directement � partir de la feuille de calcul ou d�un �l�ment personnalis� dans l�interface utilisateur.

Cette documentation ne couvre pas les fonctions XLM. Il est recommand� d�utiliser l�une des deux autres approches.
  
Pour pouvoir accéder � la fonction ou � la commande directement � partir de la feuille de calcul ou d�un �l�ment personnalis� dans l�interface utilisateur, elles doivent pr�alablement �tre inscrites aupr�s d�Excel. Pour plus d�informations sur l�inscription des commandes et des fonctions, voir [Accés au code XLL dans Excel](accessing-xll-code-in-excel.md).
  
## <a name="calling-dll-functions-and-commands-from-vba"></a>Appel des fonctions et commandes DLL à partir de VBA

Vous pouvez acc�der aux fonctions et commandes DLL dans VBA � l�aide de l�instruction **Declare**. Elle poss�de une syntaxe pour les commandes, et une syntaxe pour les fonctions.
  
- **Syntaxe 1 : commandes**

  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- **Syntaxe 2 : fonctions**

  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

Les mots cl�s facultatifs **Public** et **Private** indiquent la port�e de la fonction import�e, respectivement l�ensemble du projet Visual�Basic ou le module Visual�Basic. Le nom est celui que vous souhaitez utiliser dans le code VBA. S�il est diff�rent du nom dans DLL, vous devez utiliser le sp�cificateur Alias ��aliasname��, et vous devez indiquer le nom de la fonction comme export� par DLL. Si vous souhaitez acc�der � une fonction DLL en référence � un nombre ordinal DLL, vous devez fournir un nom d�alias, autrement dit l�ordinal pr�fix� par **#**.
  
Les commandes doivent renvoyer **void**. Les fonctions doivent renvoyer des types que VBA peut reconna�tre, **ByVal**. Cela signifie que certains types sont renvoy�s plus facilement en modifiant les arguments en place : chaînes, tableaux, types d�finis par l�utilisateur et objets.
  
> [!NOTE]
> VBA ne peut pas v�rifier que la liste d�arguments et que le renvoi indiqu� dans le module Visual�Basic sont les m�mes que ceux cod�s dans DLL. Vous devez v�rifier cet �l�ment vous-m�me tr�s attentivement, car une erreur peut provoquer un incident d�Excel.
  
Lorsque les arguments de la fonction ou de la commande ne sont pas transmis par référence ou pointeur, ils doivent �tre pr�c�d�s du mot cl� **ByVal** dans la d�claration **arglist**. Lorsqu�une fonction C/C++ prend des arguments de pointeur, ou qu�une fonction C++ prend des arguments de référence, ils doivent �tre transmis **ByRef**. Le mot cl� **ByRef** peut �tre omis des listes d�arguments, car il s�agit de la valeur par d�faut dans VBA.
  
### <a name="argument-types-in-cc-and-vba"></a>Types d’arguments dans C/C++ et VBA

Vous devez tenir compte de ce qui suit lorsque vous comparez les déclarations de types d’argument dans C/C++ et VBA.
  
- Un �l�ment **String** VBA est transmis comme pointeur vers une structure BSTR de cha�ne d�octets lorsqu�il est transmis ByVal, et comme pointeur vers un pointeur lorsqu�il est transmis **ByRef**.

- Un �l�ment **Variant** VBA contenant une cha�ne est transmis comme pointeur vers une structure BSTR de cha�ne de caract�res larges lorsqu�il est transmis **ByVal**, et comme un pointeur vers un pointeur lorsqu�il est transmis **ByRef**.

- L��l�ment **Integer** VBA est un type de 16�bits �quivalent � un �l�ment signed short dans C/C++.

- L��l�ment **Long** VBA est un type de 32�bits �quivalent � un �l�ment signed int dans C/C++.

- VBA et C/C++ permettent de d�finir des types de donn�es d�finis par l�utilisateur, � l�aide des instructions **Type** et **struct**, respectivement.

- VBA et C/C++ prennent en charge le type de donn�es **Variant**, d�fini pour C/C++ dans les fichiers d�en-t�te OLE/COM Windows en tant que VARIANT.

- Les tableaux VBA sont des �l�ments **SafeArrays** OLE d�finis pour C/C++ dans les fichiers d�en-t�te OLE/COM Windows en tant que **SAFEARRAY**.

- Le type de donn�es VBA **Currency** est transmis comme une structure de type **CY**, d�finie dans le fichier d�en-t�te Windows wtypes.h lorsqu�il est transmis **ByVal**, et comme un pointeur vers cet �l�ment lorsqu�il est transmis **ByRef**.

Dans VBA, les éléments de données dans les types de données définis par l’utilisateur sont compressés aux limites de 4 octets, tandis que dans Visual Studio, par défaut, ils sont compressés aux limites de 8 octets. Par conséquent, vous devez encadrer la définition de la structure C/C++ dans un bloc `#pragma pack(4) … #pragma pack()` pour éviter l’alignement incorrect des éléments.
  
Voici un exemple de définitions de types d’utilisateur équivalentes.
  
```vb
Type VB_User_Type
    i As Integer
    d As Double
    s As String
End Type

```

```cpp
#pragma pack(4)
struct C_user_type
{
    short iVal;
    double dVal;
    BSTR bstr; // VBA String type is a byte string
}
#pragma pack() // restore default

```

Dans certains cas, VBA prend en charge une plage de valeurs plus grande qu�Excel. Le double de VBA est compatible IEEE, et prend en charge des num�ros inf�rieurs � la normale qui sont arrondis � z�ro sur la feuille de calcul. Le type **Date** VBA peut repr�senter des dates comme 1-Jan-0100 � l�aide de dates s�rialis�es n�gatives. Excel autorise uniquement les dates s�rialis�es sup�rieures ou �gales � z�ro. Le type **Currency** VBA (un nombre de 64�bits mis � l��chelle) peut atteindre une pr�cision non prise en charge par les doubles de 8�octets, et n�est donc pas mis en correspondance dans la feuille de calcul.
  
Excel transmet uniquement des variantes des types suivants � une fonction d�finie par l�utilisateur VBA.
  
|**Type de donn�es VBA**|**Indicateurs binaires de type Variant C/C++**|**Description**|
|:-----|:-----|:-----|
|Double  <br/> |**VT_R8** <br/> ||
|Boolean  <br/> |**VT_BOOL** <br/> ||
|Date  <br/> |**VT_DATE** <br/> ||
|String  <br/> |**VT_BSTR** <br/> |Cha�ne d�octets BSTR OLE  <br/> |
|Range  <br/> |**VT_DISPATCH** <br/> |Références de plage et de cellule  <br/> |
|Variant contenant un tableau  <br/> |**VT_ARRAY** **VT_VARIANT** <br/> |Tableaux de type litt�ral  <br/> |
|Ccy  <br/> |**VT_CY** <br/> |Nombre entier de 64�bits mis � l��chelle pour autoriser 4�d�cimales de pr�cision. |
|Variant contenant une erreur  <br/> |**VT_ERROR** <br/> ||
||**VT_EMPTY** <br/> |Cellules vides ou arguments omis  <br/> |

Vous pouvez v�rifier le type d�un �l�ment Variant transmis dans VBA � l�aide de **VarType**, sauf que la fonction renvoie le type des valeurs de la plage lorsqu�elle est appel�e avec des références. Pour d�terminer si un �l�ment **Variant** est un objet de référence **Range**, vous pouvez utiliser la fonction **IsObject**.
  
Vous pouvez cr�er des �l�ments **Variants** qui contiennent des tableaux de variantes dans VBA � partir d�un �l�ment **Range** en affectant sa propri�t� **Value** � un �l�ment **Variant**. Toutes les cellules de la plage source qui sont mises en forme � l�aide du format de devise standard pour les param�tres r�gionaux en vigueur � ce moment-l� sont converties en �l�ments de tableau de type **Currency**. Toutes les cellules mises en forme en tant que dates sont converties en �l�ments de tableau de type **Date**. Les cellules contenant des chaînes sont converties en variantes **BSTR** � caract�res larges. Les cellules contenant des erreurs sont converties en �l�ments **Variants** de type **VT_ERROR**. Les cellules contenant les valeurs **Boolean** **True** ou **False** sont converties en �l�ments **Variants** de type **VT_BOOL**.
  
> [!NOTE]
> L��l�ment **Variant** stocke **True** comme -1 et **False** comme 0. Les nombres non mis en forme en tant que dates ou montants en devise sont convertis en variantes de type **VT_R8**.
  
### <a name="variant-and-string-arguments"></a>Arguments de variante et de chaîne

Excel utilise en interne des chaînes Unicode � caract�res larges. Lorsqu�une fonction d�finie par l�utilisateur VBA est d�clar�e comme prenant un argument **String**, Excel convertit la chaîne fournie en une chaîne d�octets d�une mani�re propre aux param�tres r�gionaux. Si vous souhaitez que votre fonction soit transmise � une chaîne Unicode, votre fonction d�finie par l�utilisateur VBA doit accepter un argument **Variant** au lieu d�un argument **String**. Votre fonction DLL peut ensuite accepter la chaîne � caract�res larges BSTR **Variant** � partir de VBA.
  
Pour renvoyer des chaînes Unicode vers VBA à partir d’une DLL, vous devez modifier un argument de chaîne de type **Variant** en place. Pour ce faire, vous devez déclarer la fonction DLL comme prenant un pointeur vers l’élément **Variant** et dans votre code C/C++, et déclarer l’argument dans le code VBA comme `ByRef varg As Variant`. La mémoire de l’ancienne chaîne doit être libérée, et la nouvelle valeur de chaîne créée à l’aide de la chaîne BSTR OLE ne fonctionne que dans la DLL.
  
Pour renvoyer une cha�ne d�octets � VBA � partir d�une DLL, vous devez modifier un argument BSTR de cha�ne d�octets en place. Pour ce faire, vous devez d�clarer la fonction DLL comme prenant un pointeur vers un pointeur vers l��l�ment BSTR et dans votre code C/C++, et d�clarer l�argument dans le code VBA comme **ByRef varg As String**�.
  
Vous devez g�rer uniquement les chaînes qui sont transmises de ces fa�ons � partir de VBA � l�aide des fonctions de chaîne BSTR OLE pour �viter les probl�mes li�s � la m�moire. Par exemple, vous devez appeler **SysFreeString** pour lib�rer de la m�moire avant de remplacer la chaîne transmise, et **SysAllocStringByteLen** ou **SysAllocStringLen** pour allouer de l�espace � une nouvelle chaîne.
  
Vous pouvez cr�er des erreurs de feuille de calcul Excel en tant que **Variants** dans VBA � l�aide de la fonction **CVerr** avec des arguments, comme indiqu� dans le tableau suivant. Les erreurs de feuille de calcul peuvent �galement �tre renvoy�es � VBA � partir d�une DLL � l�aide d��l�ments **Variants** de type **VT_ERROR**, et avec les valeurs suivantes dans le champ **ulVal**.
  
|**Erreur**|**Valeur de type Variant ulVal**|**Argument CVerr**|
|:-----|:-----|:-----|
|#NULL!  <br/> |2148141008  <br/> |2000  <br/> |
|#DIV/0!  <br/> |2148141015  <br/> |2007  <br/> |
|#VALUE!  <br/> |2148141023  <br/> |2015  <br/> |
|#REF!  <br/> |2148141031  <br/> |2023  <br/> |
|#NAME ?  <br/> |2148141037  <br/> |2029  <br/> |
|#NUM!  <br/> |2148141044  <br/> |2036  <br/> |
|#N/A  <br/> |2148141050  <br/> |2042  <br/> |

La valeur variante **ulVal** indiquée équivaut à la valeur d’argument **CVerr** et à la valeur hexadécimale x800A0000.
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a>Appel de fonctions DLL directement à partir de la feuille de calcul

Vous ne pouvez pas acc�der aux fonctions DLL�Win32 � partir de la feuille de calcul sans, par exemple, utiliser VBA ou XLM comme interfaces, ou sans informer Excel � l�avance de la fonction, de ses arguments et de son type de renvoi. Le processus de cette op�ration est appel� l�inscription.
  
Vous pouvez acc�der aux fonctions d�une DLL dans la feuille de calcul � l�aide des m�thodes suivantes :
  
- d�clarez la fonction dans VBA comme d�crit pr�c�demment, et acc�dez-y via une fonction d�finie par l�utilisateur VBA�;

- appelez la fonction DLL � l�aide de l��l�ment CALL sur une feuille macro XLM, et acc�dez-y via une fonction d�finie par l�utilisateur XML�;

- utilisez une commande XML ou VBA pour appeler la fonction **REGISTER** XML, qui fournit les informations dont Excel a besoin pour reconna�tre la fonction lorsqu�elle est saisie dans une cellule de feuille de calcul�;

- transformez la DLL en un �l�ment XLL et inscrivez la fonction � l�aide de la fonction **xlfRegister** d�API C lorsque XLL est activ�.

La quatri�me approche est autonome : le code qui inscrit les fonctions et le code de fonction sont contenus dans le m�me projet de code. Le fait d�apporter des modifications au compl�ment n�implique pas la modification d�une feuille XML ou d�un module de code VBA. Pour proc�der de fa�on organis�e tout en restant dans le cadre des fonctionnalit�s de l�API C, vous devez convertir votre DLL en un �l�ment XLL, et charger le compl�ment obtenu � l�aide du gestionnaire de compl�ments. Cela permet � Excel d�appeler une fonction que votre DLL expose lorsque le compl�ment est charg� ou activ�. � partir de cette �tape, vous pouvez enregistrer toutes les fonctions que contient votre XLL et ex�cuter toute autre initialisation DLL.
  
## <a name="calling-dll-commands-directly-from-excel"></a>Appel de commandes DLL directement à partir d’Excel

Les commandes DLL�Win32 ne sont pas accessibles directement � partir des menus et bo�tes de dialogue Excel sans avoir une interface, telle que VBA, ou sans avoir inscrit les commandes � l�avance.
  
Vous pouvez acc�der aux commandes d�une DLL � l�aide des m�thodes suivantes :
  
- d�clarez la commande dans VBA comme d�crit pr�c�demment, et acc�dez-y via une macro VBA�;

- appelez la commande DLL � l�aide de l��l�ment **CALL** sur une feuille macro XLM, et acc�dez-y via une macro XML�;

- utilisez une commande XML ou VBA pour appeler la fonction **REGISTER** XML, qui fournit les informations dont Excel a besoin pour reconna�tre la commande lorsqu�elle est saisie dans une bo�te de dialogue qui attend le nom d�une commande de macro�;

- transformez la DLL en un �l�ment XLL et inscrivez la commande � l�aide de la fonction **xlfRegister** d�API C.

Comme expliqu� plus haut dans le contexte des fonctions DLL, la quatri�me approche est la plus autonome, et conserve le code d�inscription proche du code de la commande. Pour r�aliser cette action, vous devez convertir votre DLL en un �l�ment XLL et charger le compl�ment obtenu � l�aide du gestionnaire de compl�ments. Le fait d�inscrire des commandes de cette fa�on vous permet �galement d�attacher la commande � un �l�ment de l�interface utilisateur, tel qu�un menu personnalis�, ou de configurer une interruption d��v�nement qui appelle la commande suite � une combinaison de touches donn�e ou � un autre �v�nement.
  
Toutes les commandes XLL inscrites aupr�s d�Excel sont consid�r�es comme �tant au format suivant.
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> Excel ignore la valeur de renvoi, sauf si elle est appel�e � partir d�une feuille macro XLM, auquel cas la valeur de retour est convertie en **TRUE** ou **FALSE**. Vous devez par cons�quent renvoyer 1 si votre commande a �t� ex�cut�e correctement, et 0 si elle a �chou� ou a �t� annul�e par l�utilisateur.
  
## <a name="dll-memory-and-multiple-dll-instances"></a>Mémoire DLL et instances multiples DLL

Lorsqu�une application charge une DLL, le code ex�cutable de la DLL est charg� dans le segment de m�moire global afin que vous puissiez l�ex�cuter, et de l�espace est allou� sur le segment de m�moire global pour ses structures de donn�es. Windows utilise le mappage de m�moire pour afficher ces zones de m�moire comme si elles faisaient partie du processus de l�application, de fa�on � ce que l�application puisse y acc�der.
  
Si une deuxi�me application charge ensuite la DLL, Windows ne r�alise pas une autre copie du code ex�cutable DLL, car cette m�moire est en lecture seule. Windows mappe la m�moire du code ex�cutable DLL aux processus des deux applications. Toutefois, il alloue un deuxi�me espace pour une copie priv�e des structures de donn�es de la DLL, et mappe cette copie au deuxi�me processus uniquement. Cela garantit qu�aucune application ne peut interf�rer avec les donn�es de la DLL de l�autre application.
  
Cela signifie que les d�veloppeurs DLL n�ont pas � se pr�occuper des variables statiques et globales, ni des structures de donn�es utilis�es par plusieurs applications, ou plusieurs instances de la m�me application. Chaque instance de chaque application obtient sa propre copie des donn�es de la DLL.
  
Les d�veloppeurs DLL doivent �tre concern�s par la m�me instance d�une application en appelant leur DLL plusieurs fois � partir de diff�rents threads, car cela peut entra�ner un conflit pour les donn�es de cette instance. Pour plus d�informations, voir [Gestion de la m�moire dans Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Voir aussi

- [Développement des fichiers DLL](developing-dlls.md)
- [Appel dans Excel � partir du fichier DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md)
