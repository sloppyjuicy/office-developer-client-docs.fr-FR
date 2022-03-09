---
title: xlfRegister (formulaire 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- fonction xlfregister [excel 2007]
ms.localizationpriority: medium
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
ms.openlocfilehash: 12ec5575796ba7e342553f172e56390f407fd059
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373794"
---
# <a name="xlfregister-form-1"></a>xlfRegister (formulaire 1)

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Peut être appelée à partir d’une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel. Cela équivaut à appeler **REGISTER** à partir d’Excel feuille macro XLM.
  
**xlfRegister peut** être appelé sous deux formes :
  
- xlfRegister (formulaire 1) : inscrit une seule commande ou fonction.

- [xlfRegister (formulaire 2)](xlfregister-form-2.md) : charge et active une XLL.

Appelée dans le formulaire 1, cette fonction met une fonction ou commande DLL à la disposition de Excel, définit son nombre d’utilisations sur 1 et renvoie son ID d’inscription, qui peut être utilisé pour appeler la fonction ultérieurement à l’aide de la fonction [xlUDF](xludf.md) ou **xlfCall**. L’ID d’inscription est également utilisé pour désinsister la fonction à l’aide [de xlfUnregister (formulaire 1).](xlfunregister-form-1.md) Si la fonction a été inscrite, l’appel **de xlfRegister** à nouveau incrémente son nombre d’utilisations.
  
Cette forme de la fonction définit également un nom masqué qui est l’argument de texte de la fonction, _pxFunctionText_, et qui évalue l’ID d’inscription de la fonction ou de la commande. Lorsque vous désinssez la fonction, supprimez ce nom à l’aide [de xlfSetName](xlfsetname.md). Pour plus d’informations, reportez-vous à la rubrique [Problèmes connus concernant le développement de XLL Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, int iCount,
    LPXLOPER12 pxModuleText,   LPXLOPER12 pxProcedure,
    LPXLOPER12 pxTypeText,     LPXLOPER12 pxFunctionText,
    LPXLOPER12 pxArgumentText, LPXLOPER12 pxMacroType,
    LPXLOPER12 pxCategory,     LPXLOPER12 pxShortcutText,
    LPXLOPER12 pxHelpTopic,    LPXLOPER12 pxFunctionHelp,
    LPXLOPER12 pxArgumentHelp1, LPXLOPER12 pxArgumentHelp2,
        ...);
```

## <a name="parameters"></a>Paramètres

_pxModuleText_ (**xltypeStr**)
  
Nom de la DLL qui contient la fonction. Cela peut être obtenu en appelant la fonction XLL uniquement [xlGetName](xlgetname.md) si la fonction inscrite se trouve également dans la DLL en cours d’exécution.
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
S’il s’agit d’une chaîne, le nom de la fonction à appeler tel qu’il apparaît dans le code DLL. S’il s’agit d’un nombre, il s’agit du numéro d’exportation ordinal de la fonction à appeler. Pour plus de clarté, utilisez toujours la forme de chaîne.
  
_pxTypeText_ (**xltypeStr**)
  
Chaîne facultative qui spécifie les types d’arguments de la fonction et le type de la valeur de retour de la fonction. Pour plus d'informations, voir la section Notes. Cet argument peut être omis pour une DLL (XLL) autonome qui inclut une fonction [xlAutoRegister](xlautoregister-xlautoregister12.md) ou **xlAutoRegister12**.
  
> [!NOTE]
> **XlAutoRegister12 est** uniquement pris en charge dans Excel 2007.
  
Si **xlfRegister** est appelé avec cet argument manquant, Excel appelle **xlAutoRegister** ou **xlAutoRegister12**, s’il existe dans la DLL spécifiée, qui doit ensuite enregistrer correctement la fonction en fournissant ces informations.
  
_pxFunctionText_ (**xltypeStr**)
  
Nom de la fonction tel qu’il apparaîtra dans l’Assistant Fonction. Cet argument est facultatif ; Si elle est omise, la fonction n’est pas disponible dans l’Assistant Fonction et peut uniquement être appelée à l’aide de la fonction **CALL** à l’aide de l’ID d’inscription des fonctions à partir d’une feuille macro XLM. Par conséquent, pour une utilisation de feuille de calcul ordinaire, vous devez gérer cet argument selon les besoins.
  
_pxArgumentText_ (**xltypeStr**)
  
Chaîne de texte facultative qui décrit les arguments de la fonction. L’utilisateur voit cela dans l’Assistant Fonction. S’il est omis, Excel des descriptions de base à partir _de pxTypeText_.
  
_pxMacroType_ (**xltypeNum** ou **xltypeInt**)
  
Argument facultatif qui indique le type de point d’entrée XLL. La valeur par défaut, si elle est omise, est 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _Valeur pxMacroType_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Peut être appelé à partir d’une feuille de calcul  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Peut être appelé à partir d’une feuille macro  <br/> |Oui  <br/> |Oui  <br/> |Oui  <br/> |
|Peut être appelée à partir d’une définition de nom défini  <br/> |Oui  <br/> |Oui  <br/> |Oui  <br/> |
|Peut être appelée à partir d’une expression de mise en forme conditionnelle  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Répertorié dans l’Assistant Fonction pour les fonctions de feuille de calcul  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Répertorié dans l’Assistant Fonction pour les fonctions de feuille macro  <br/> |Non  <br/> |Oui  <br/> |Oui  <br/> |

Dans la pratique, vous devez utiliser 1 pour les fonctions de feuille de calcul, 1 pour les fonctions équivalentes à une feuille macro (inscrites en tant que type **#**) que vous souhaitez appeler à partir de la feuille de calcul et 2 pour les commandes.
  
> [!NOTE]
> Les commandes XLL sont masquées et ne sont pas affichées dans les boîtes de dialogue pour l’exécution des macros, bien que leur nom puisse être entré n’importe où, un nom de commande valide est requis.
  
_pxCategory_ (**xltypeStr** ou **xltypeNum**)
  
Argument facultatif qui vous permet de spécifier la catégorie à laquelle la nouvelle fonction ou commande doit appartenir. L’Assistant Fonction divise les fonctions par type (catégorie). Vous pouvez spécifier un nom de catégorie ou un numéro séquentiel, où le numéro est la position dans laquelle la catégorie apparaît dans l’Assistant Fonction. Pour plus d’informations, voir la section « Noms des catégories ». Si elle est omise, la catégorie définie par l’utilisateur est supposée.
  
_pxShortcutText_ (**xltypeStr**)
  
Chaîne d’un caractère, sensible à la cas, qui spécifie la touche de contrôle affectée à cette commande. Par exemple, « A » affecte cette commande à CONTROL+Shift+A. Cet argument est facultatif et est utilisé uniquement pour les commandes.
  
_pxHelpTopic_ (**xltypeStr**)
  
Référence facultative au fichier d’aide (.chm ou .hlp) à afficher lorsque l’utilisateur clique sur le bouton Aide (lorsque votre fonction personnalisée est affichée). Peut être dans le formulaire `filepath!HelpContextID` ou `https://address/path_to_file_in_site!0`. Les deux parties avant et après le « ! » sont requises. _HelpContextID_ ne doit pas contenir de guillemets simples et sera converti par Excel en un octet non signé de 4 octets de long, sous la forme décimale. Lorsque vous utilisez le formulaire d’URL, Excel ouvre uniquement le fichier d’aide référencé.
  
_pxFunctionHelp_ (**xltypeStr**)
  
Chaîne facultative qui décrit votre fonction personnalisée lorsqu’elle est sélectionnée dans l’Assistant Fonction.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Facultatif. Première des chaînes qui décrivent les arguments personnalisés de la fonction lorsque la fonction est sélectionnée dans l’Assistant Fonction. Dans Excel 2003 et les antérieures, **xlfRegister** peut prendre, au maximum, 30 arguments afin que vous pouvez fournir cette aide pour les 20 premiers arguments de votre fonction uniquement. À compter Excel 2007, **xlfRegister** peut prendre jusqu’à 255 arguments afin que vous pouvez fournir cette aide pour jusqu’à 245 paramètres de fonction.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si l’inscription a réussi, cette fonction renvoie l’ID de registre de la fonction (**xltypeNum**), qui peut être utilisé dans les appels à **xlUDF** et **xlfUnregister** dans une DLL, ou avec **CALL** et **UNREGISTER** dans une feuille macro XLM. Sinon, elle renvoie une #VALUE! erreur.
  
## <a name="remarks"></a>Remarques

### <a name="data-types"></a>Types de données

_L’argument pxTypeText_ spécifie le type de données de la valeur de retour et les types de données de tous les arguments de la fonction DLL ou de la ressource de code. Le premier caractère de _pxTypeText_ spécifie le type de données de la valeur de retour. Les caractères restants indiquent les types de données de tous les arguments. Par exemple, une fonction DLL qui renvoie un nombre à pointe flottante et prend un nombre d’un nombre integer et un nombre à point flottant comme arguments nécessiterait « BRÉ » pour l’argument _pxTypeText_ .
  
Les types de données et les structures utilisés par Excel pour échanger des données avec des XL sont résumés dans les deux tableaux suivants.
  
Le premier tableau répertorie les types pris en charge dans toutes les versions de Excel.
  
|**Type de données**|**Passer par valeur**|**Passer par référence (pointeur)**|**Comments**|
|:-----|:-----|:-----|:-----|
|Booléen  <br/> |A  <br/> |L  <br/> |short [int] (0=false ou 1=true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |Chaîne d’octets ASCII se terminant par null  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Chaîne d’byte ASCII comptée  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD 16 bits  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |Integer signé 16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |Integer signé 32 bits  <br/> |
|FP  <br/> ||K  <br/> |Structure de tableau à virgule flottante  <br/> |
|Tableau  <br/> ||O  <br/> |Trois arguments sont passés :<br/>- unsigned short int \*<br/>- unsigned short int \*<br/>- double []  <br/> |
|XLOPER  <br/> ||P  <br/> |Tableaux et valeurs de feuille de calcul de type variable  <br/> |
|||R  <br/> |Valeurs, tableaux et références de plage  <br/> |

Dans Excel 2007, les types de données suivants ont été introduits pour prendre en charge les grilles plus grandes et les chaînes Unicode longues.
  
|**Type de données**|**Passer par valeur**|**Passer par référence (pointeur)**|**Comments**|
|:-----|:-----|:-----|:-----|
|unsigned short \*  <br/> ||C%, F%  <br/> |Chaîne de caractères larges Unicode terminée par null  <br/> |
|unsigned short \*  <br/> ||D%, G%  <br/> |Chaîne de caractères larges Unicode comptée  <br/> |
|FP12  <br/> ||K%  <br/> |Structure de tableau à grande grille à pointe flottante  <br/> |
|Tableau  <br/> ||O%  <br/> |Trois arguments sont passés :<br/>- signed int \* /RW \*<br/>- signed int \* /COL \*<br/>- double []  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Tableaux et valeurs de feuille de calcul de type variable  <br/> |
|||U  <br/> |Valeurs, tableaux et références de plage  <br/> |

À compter Excel 2010, les types de données suivants ont été introduits :
  
|**Type de données**|**Passer par valeur**|**Passer par référence (pointeur)**|**Comments**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |Le handle asynchrone est utilisé pour suivre un appel de fonction asynchrone en attente par Excel et le XLL.L’existence du type de paramètre dans la chaîne de type désigne également la fonction comme asynchrone. Pour plus d’informations sur les fonctions [asynchrones, voir Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md). |

Les types de chaînes **F**, **F%**, **G** et **G%** sont utilisés pour les arguments qui sont modifiés directement (modified-in-place).
  
Lorsque vous travaillez avec les types de données affichés dans le tableau précédent, ez compte des informations suivantes :
  
- Les déclarations en langage C supposent que votre compilateur utilise des nombres doubles de 8 byte, des nombres courts de 2 to et des nombres longs de 4 to par défaut.
- Toutes les fonctions dans les DLLs et les ressources de code sont appelées à l’aide **__stdcall** convention d’appel.
- Toute fonction qui renvoie un type de données par référence, c’est-à-dire qui renvoie un pointeur vers quelque chose, peut renvoyer en toute sécurité un pointeur Null. Excel interprète un pointeur null comme un #NUM ! erreur.

## <a name="additional-data-type-information"></a>Informations supplémentaires sur le type de données

Cette section contient des informations détaillées sur les types de données **E**, **F**, **F%**, **G**, **G%**, **K**, **O**, **P**, **Q**, **R** et **U** , ainsi que d’autres informations sur l’argument _pxTypeText_ .
  
### <a name="e-data-type"></a>Type de données E

Excel s’attend à ce qu’une DLL utilisant le type de données E passe des pointeurs vers des nombres à flottant sur la pile. Cela peut entraîner des problèmes avec certaines langues (par exemple, Borland C++) qui s’attendent à ce que le nombre soit transmis sur la pile de l’émulateur de coprocesseur. La solution de contournement consiste à transmettre un pointeur au nombre sur la pile de coprocesseurs. L’exemple suivant montre comment renvoyer un double de Borland C++.
  
```cpp
typedef double * lpDbl;
extern "C" lpDbl __stdcall AddDbl(double D1,
    double D2, WORD npDbl)
{
    lpDbl Result;
    Result = (lpDbl)MK_FP(_SS, npDbl);
    *Result = D1 + D2;
    return (Result);
}
```

### <a name="f-f-g-and-g-data-types"></a>Types de données F, F%, G et G%

Avec les types **de données F**, **F%**, **G** et **G%**, une fonction peut modifier une mémoire tampon de chaîne qui est allouée par Excel. Si le code de type de valeur renvoyée est l’un de ces types, Excel ignore la valeur renvoyée par la fonction. Au lieu de cela, Excel recherche la liste des arguments de fonction pour le premier type de données correspondant (**F**, **F%**, **G** ou **G%**), puis prend le contenu actuel de la mémoire tampon de chaîne allouée comme valeur de retour. Toutes les versions de Excel allouent 256 octets pour les chaînes **F** et **G** ASCII, et à partir de Excel 2007, 65 536 octets sont alloués, suffisamment pour 32 768 caractères Unicode, pour les chaînes Unicode **F%** et **G%.** N’oubliez pas que les mémoires tampons doivent inclure un nombre de caractères (types **G** et **G%**) ou un caractère de terminaison null (types **F** et **F%**), afin que les longueurs de chaîne maximales réelles soient de 255 et 32 767. Les chaînes Unicode, et par conséquent les arguments **F%** et **G%**, sont disponibles uniquement par le biais de l’API C Excel.
  
### <a name="k-and-k-data-types"></a>Types de données K et K%

Les types **de données K** et **K%** utilisent respectivement des pointeurs vers les structures FP et FP12 de taille variable. Ces structures sont définies dans XLLCALL.H. Les structures FP12, et par conséquent les arguments **de type K%**, sont uniquement pris en charge à partir Excel 2007.
  
### <a name="o-and-o-data-types"></a>Types de données O et O%

Les types de données **O** et **O%** ne peuvent être utilisés que pour les arguments, et non pour renvoyer des valeurs, bien que les valeurs soient renvoyées en modifiant un argument de type **O** ou **O%** en place. Chacun passe trois éléments : un pointeur vers le nombre de lignes dans un tableau, un pointeur vers le nombre de colonnes dans un tableau et un pointeur vers un tableau à deux dimensions de nombres à valeur flottante.
  
Pour modifier un tableau transmis par le type de données O ou O% en place, vous pouvez utiliser « >O » ou « >O% » comme argument _pxTypeText_ . Pour plus d’informations sur la modification d’un tableau, voir la section « Modification sur place : fonctions déclarées comme vides » dans cette rubrique.
  
Le type **de données O** a été créé pour une compatibilité directe avec les DLL Fortran, qui passent des arguments par référence.
  
Le **%O%** est pris en charge Excel 2007 et prend en charge le plus grand nombre de lignes Excel prise en charge.
  
### <a name="p-and-q-data-types"></a>Types de données P et Q

Lorsque les arguments de fonction DLL sont enregistrés comme prenant le type **P** XLOPERs ou **Q** XLOPER12, Excel convertit les références à cellule unique en valeurs simples et les références à plusieurs cellules en tableaux lors de la préparation de ces arguments. En d’autres termes, les types **P** et **Q** arrivent toujours dans votre fonction en tant que l’un de ces types : **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing** ou **xltypeNil**, mais pas **xltypeRef** ou **xltypeSRef** , car ils sont toujours déférences. **XlOPER12s**, et par conséquent les arguments **de type Q**, sont uniquement pris en charge à partir Excel 2007.
  
Si les types **xltypeMissing** ou **xltypeNil** sont utilisés pour les valeurs de retour, ils sont interprétés par Excel comme zéro numérique. **xltypeMissing** est transmis lorsque l’appelant omet un argument. **XltypeNil est** transmis lorsque l’appelant transmet une référence à une cellule vide. Lorsqu’une plage de cellules est convertie en **xltypeMulti** à passer en tant que type **P** ou **Q**, toutes les cellules vides de la plage sont converties en éléments de tableau **xltypeNil** . Les éléments manquants dans un tableau littéral sont passés de la même manière que les **éléments xltypeNil** .
  
### <a name="volatile-functions-and-recalculation"></a>Fonctions volatiles et recalcul

Dans une feuille de calcul, vous pouvez rendre une fonction DLL ou une ressource de code volatile, afin qu’elle recalcule chaque fois que la feuille de calcul est recalculée. Pour ce faire, ajoutez un point d’exclamation (!) après le dernier code d’argument dans l’argument _pxTypeText_ .

> [!NOTE]
> Par défaut, les fonctions qui prennent le type **R** XLOPERs ou **U** XLOPER12 et qui sont enregistrées en tant qu’équivalents de feuille macro (type **#**; voir section suivante) sont traitées comme volatiles dans Excel.
  
### <a name="functions-declared-as-void"></a>Fonctions déclarées comme nulles

Il existe deux cas qui appellent la déclaration d’une fonction comme renvoyant void. Dans les deux cas, la fonction renvoie son résultat par d’autres moyens.
  
#### <a name="modifying-in-place"></a>Modification sur place

Vous pouvez utiliser un chiffre _unique n_ pour le code de type de retour dans _pxTypeText_, où _n_ est un nombre de 1 à 9. Cela Excel de prendre la valeur de la variable à l’emplacement pointé par l’argument _n_th’in_pxTypeText_as la valeur de retour. C’est également ce que l’on appelle la modification sur place. The_n_th argument doit être un type de données pass-by-reference (C, D, E, F%, G, G%, K, K%, L, M, N, O,O%, P, Q, R ou U). La fonction DLL ou la ressource de code doit également être déclarée avec le mot clé **void** dans les langages C/C++  (ou le mot clé de procédure dans le langage Pascal).
  
Par exemple, une fonction DLL qui prend une chaîne terminée par null et deux pointeurs vers des integers en tant qu’arguments peut modifier la chaîne en place. Utilisez « 1FMM » comme argument _pxTypeText_ et déclarez la fonction comme nulle.
  
Les versions précédentes de Excel **\>** utilisées au début de _pxTypeText_ pour signifier que la fonction a été déclarée comme nulle et que le premier argument devait être modifié sur place, il n’y avait aucun moyen de modifier un argument autre que le premier. L’équivalent **\>** de _n_ = 1 dans les versions Excel actuelles **\>** et cette utilisation dans les fonctions synchrones est uniquement prise en charge pour la compatibilité ascendante.

#### <a name="asynchronous-functions"></a>Fonctions asynchrones

Une fonction asynchrone, notée à l’aide d’un paramètre de type X dans **pxTypeText**, ne retourne pas son résultat à partir de l’appel de fonction initial. Au lieu de cela, vous devez déclarer une fonction asynchrone comme nulle, puis le add-in renvoie le résultat par le biais d’un rappel. La fonction asynchrone doit être inscrite au **\>** début de **pxTypeText**. Dans les fonctions asynchrones, **\>** indique que la fonction est déclarée comme nulle, mais n’indique pas que le premier argument est modifié en place. Pour plus d’informations sur les fonctions [asynchrones, voir Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Inscription des fonctions de feuille de calcul en tant qu’équivalents de feuille macro (gestion des cellules non calculées)

Placer un **#** caractère après le dernier code de paramètre dans _pxTypeText_ donne à la fonction les mêmes autorisations d’appel que les fonctions sur une feuille macro. Elle comprennent notamment :
  
- La fonction peut récupérer les valeurs des cellules qui n’ont pas encore été calculées dans ce cycle de recalcul.

- La fonction peut appeler n’importe quelle fonction d’informations XLM (classe 2), par exemple **, xlfGetCell**.

- Si le signe nombre (#) n’est pas présent : l’évaluation d’une cellule non calculée entraîne une erreur **xlretUncalced** , et la fonction actuelle est rappelée une fois que la cellule a été calculée ; L’appel d’une fonction d’informations XLM autre que **xlfCaller** entraîne une **erreur xlretInvXlfn** .

### <a name="registering-worksheet-functions-as-thread-safe"></a>Inscription de fonctions de feuille de calcul comme thread-safe

À compter Excel 2007, Excel peut effectuer un recalcul de workbook multithread. Cela signifie qu’il peut affecter différentes instances d’une fonction thread-safe à des threads simultanés pour la réévaluation. À compter Excel 2007, la plupart des fonctions de feuille de calcul intégrées sont thread-safe. À compter Excel 2007, Excel permet également aux XL d’inscrire des fonctions de feuille de calcul en tant que fonctions thread-safe. Pour ce faire, incluez un caractère **$** après le dernier code de paramètre _dans pxTypeText_.
  
> [!NOTE]
> Seules les fonctions de feuille de calcul peuvent être déclarées comme thread-safe. Excel ne considère pas qu’une fonction équivalente à une feuille macro soit thread-safe, de sorte que vous ne pouvez pas l’appender **#** **$** à la fois et des caractères à l’argument _pxTypeText_.
  
Si vous avez inscrit une fonction comme thread-safe, vous devez vous assurer qu’elle se comporte de manière thread-safe, bien que Excel rejette tous les appels thread-unsafe via l’API C. Par exemple, si une fonction thread-safe tente d’appeler **xlfGetCell**, l’appel échoue avec l’erreur **xlretNotThreadSafe** .
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Inscription des fonctions de feuille de calcul en tant que cluster-safe

À compter Excel 2010, Excel pouvez décharger les appels de fonction vers un fournisseur de cluster de calcul désigné. Pour plus d’informations, [voir Cluster Coffre Functions](cluster-safe-functions.md). Toutes les fonctions de feuille de calcul XLL inscrites en tant que cluster-safe prennent part au déchargement si un cluster est disponible. Les fonctions sécurisées pour le cluster **&amp;** sont enregistrées en incluant le caractère après le dernier code de paramètre dans l’argument _pxTypeText_ .
  
Si vous avez inscrit une fonction en tant que cluster-safe, vous devez vous assurer qu’elle se comporte de manière sécurisée pour le cluster. Pour plus d’informations, [voir Cluster Coffre Functions](cluster-safe-functions.md).
  
> [!NOTE]
> Seules les fonctions de feuille de calcul peuvent être déclarées comme cluster-safe. Excel ne considère pas qu’une fonction équivalente à une feuille macro soit sécurisée en cluster, de sorte que vous ne pouvez pas y appender **#** **&amp;** les caractères et les deux à l’argument _pxTypeText_. Les fonctions de feuille de calcul peuvent être déclarées à la fois comme cluster-safe et thread-safe. Dans ce cas, Excel permet à ces fonctions de prendre part au recalcul multithread lorsque le déchargement de cluster est désactivé.
  
### <a name="category-names"></a>Noms de catégorie

Utilisez les instructions suivantes pour déterminer la catégorie dans laquelle placer vos fonctions XLL.
  
- Si la fonction fait une chose qui pourrait être effectuée par l’utilisateur dans le cadre de l’interface utilisateur de votre add-in, vous devez placer la fonction dans la **catégorie Commandes** .
- Si la fonction renvoie des informations sur l’état du module complémentaire ou toute autre information utile, vous devez placer la fonction dans la **catégorie Informations** .
- Un add-in ne doit jamais ajouter de fonctions ou de commandes à la **catégorie Définie par l’utilisateur** . Cette catégorie est pour l’utilisation exclusive des utilisateurs finaux.

-La catégorie est spécifiée à l’aide du _paramètre pxCategory_ pour **xlfRegister**. Il peut s’agit d’un nombre ou d’un texte qui correspond à l’une des catégories standard codées en dur ou du texte d’une nouvelle catégorie spécifiée par la DLL. Si le texte donné n’existe pas encore, Excel crée une catégorie avec ce nom.
  
Le tableau suivant répertorie les catégories standard qui sont visibles  lorsque vous affichez la boîte de dialogue Coller une fonction à partir d’une feuille de calcul.
  
|**Number**|**Text**|
|:-----|:-----|
|1  <br/> |Financier  <br/> |
|2  <br/> |Heure de &amp; la date  <br/> |
|3  <br/> |Math &amp; Trig  <br/> |
|4  <br/> |Texte  <br/> |
|5  <br/> |Logique  <br/> |
|6   <br/> |Lookup &amp; Reference  <br/> |
|7   <br/> |Database  <br/> |
|8   <br/> |Statistiques  <br/> |
|9   <br/> |Informations  <br/> |
|14   <br/> |Personnalisées  <br/> |
||Ingénierie (depuis Excel 2007)  <br/> |
||Cube (à compter Excel 2007)  <br/> |

En outre, ces catégories sont également visibles lorsque vous affichez la boîte de dialogue Coller une fonction à partir d’une feuille macro.
  
|**Number**|**Text**|
|:-----|:-----|
|10  <br/> |Commandes  <br/> |
|11  <br/> |DDE/Externe  <br/> |
|12   <br/> |Personnalisation  <br/> |
|13  <br/> |Contrôle de macros  <br/> |

### <a name="example"></a>Exemple

Consultez le code de la **fonction xlAutoOpen** dans  `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Voir aussi

- [REGISTER.ID](xlfregisterid.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)
