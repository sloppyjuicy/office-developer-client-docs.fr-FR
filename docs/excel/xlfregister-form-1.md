---
title: xlfRegister (formulaire 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- fonction xlfRegister [Excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3cd2e5072c8602fe301028e69592220a8345c211
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303863"
---
# <a name="xlfregister-form-1"></a>xlfRegister (formulaire 1)

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d'une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel. Cela équivaut à appeler **Register** à partir d'une feuille macro XLM Excel. 
  
**xlfRegister** peut être appelé sous deux formes: 
  
- xlfRegister (formulaire 1): inscrit une commande ou une fonction unique.
    
- [xlfRegister (formulaire 2)](xlfregister-form-2.md): charge et active un XLL.
    
Appelée dans le formulaire 1, cette fonction rend une fonction ou commande DLL disponible dans Excel, définit son nombre d'utilisations sur 1 et renvoie son ID d'inscription, qui peut être utilisé pour appeler la fonction ultérieurement à l'aide de l' [xlUDF](xludf.md) ou de la fonction **xlfCall** . L'ID d'inscription est également utilisé pour annuler l'inscription de la fonction à l'aide de [xlfUnregister (formulaire 1)](xlfunregister-form-1.md). Si la fonction a été inscrite, l'appel de **xlfRegister** incrémente son nombre d'utilisations. 
  
Cette forme de la fonction définit également un nom masqué correspondant à l'argument texte de la fonction, _pxFunctionText_, et correspond à l'ID d'enregistrement de la fonction ou de la commande. Lorsque vous annulez l'inscription de la fonction, supprimez ce nom à l'aide du [xlfSetName](xlfsetname.md). Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).
  
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
  
Nom de la DLL qui contient la fonction. Cela peut être obtenu en appelant la fonction XLL-only [xlGetName](xlgetname.md) si la fonction inscrite se trouve également dans la dll en cours d'exécution. 
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
S'il s'agit d'une chaîne, le nom de la fonction à appeler telle qu'elle apparaît dans le code de la DLL. S'il s'agit d'un nombre, le numéro d'export ordinal de la fonction à appeler. Pour plus de clarté, utilisez toujours le formulaire de chaîne.
  
_pxTypeText_ (**xltypeStr**)
  
Chaîne facultative qui spécifie les types d'arguments de la fonction et le type de la valeur de retour de la fonction. Pour plus d'informations, consultez la section Notes. Cet argument peut être omis pour une DLL autonome (XLL) qui inclut une [fonction xlAutoRegister](xlautoregister-xlautoregister12.md) ou **xlAutoRegister12**. 
  
> [!NOTE]
> **xlAutoRegister12** est uniquement pris en charge dans Excel 2007. 
  
Si **xlfRegister** est appelé avec cet argument manquant, Excel appelle **xlAutoRegister** ou **xlAutoRegister12**, s'il existe dans la DLL spécifiée, qui doit ensuite correctement enregistrer la fonction en fournissant ces informations.
  
_pxFunctionText_ (**xltypeStr**)
  
Nom de la fonction tel qu'il apparaîtra dans l'Assistant fonction. Cet argument est facultatif; Si elle est omise, la fonction n'est pas disponible dans l'Assistant fonction et ne peut être appelée qu'à l'aide de la fonction **Call** à l'aide de l'ID d'enregistrement des fonctions d'une feuille macro XLM. Par conséquent, pour une utilisation ordinaire de feuille de calcul, vous devez gérer cet argument comme requis. 
  
_pxArgumentText_ (**xltypeStr**)
  
Chaîne de texte facultative qui décrit les arguments de la fonction. L'utilisateur voit cela dans l'Assistant fonction. Si ce paramètre est omis, Excel construit des descriptions de base à partir de _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** ou **xltypeInt**)
  
Argument facultatif qui indique le type de point d'entrée XLL. La valeur par défaut, si elle est omise, est 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _valeur pxMacroType_ <br/> |0  <br/> |0,1  <br/> |n°2  <br/> |
|Peut être appelé à partir d'une feuille de calcul  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Peut être appelé à partir d'une feuille macro  <br/> |Oui  <br/> |Oui  <br/> |Oui  <br/> |
|Peut être appelé à partir d'une définition de nom définie  <br/> |Oui  <br/> |Oui  <br/> |Oui  <br/> |
|Peut être appelé à partir d'une expression de mise en forme conditionnelle  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Mentionné dans l'Assistant fonction pour les fonctions de feuille de calcul  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Dans l'Assistant fonction pour les fonctions de feuille macro  <br/> |Non  <br/> |Oui  <br/> |Oui  <br/> |
   
Dans la pratique, vous devez utiliser 1 pour les fonctions de feuille de calcul, 1 pour les fonctions équivalentes de feuille macro (inscrites en tant que type **#**) que vous souhaitez appeler à partir de la feuille de calcul, et 2 pour les commandes. 
  
> [!NOTE]
> Les commandes XLL sont masquées et ne sont pas affichées dans les boîtes de dialogue pour l'exécution des macros, bien qu'il soit possible d'entrer leurs noms partout où un nom de commande valide est requis. 
  
_pxCategory_ (**xltypeStr** ou **xltypeNum**)
  
Argument facultatif qui vous permet de spécifier la catégorie à laquelle la nouvelle fonction ou commande doit appartenir. L'Assistant fonction divise les fonctions par type (Category). Vous pouvez spécifier un nom de catégorie ou un numéro séquentiel, où le nombre correspond à la position dans laquelle la catégorie apparaît dans l'Assistant fonction. Pour plus d'informations, reportez-vous à la section «noms de catégorie». Si ce paramètre est omis, la catégorie définie par l'utilisateur est supposée.
  
_pxShortcutText_ (**xltypeStr**)
  
Chaîne qui respecte la casse d'un caractère, qui spécifie la touche de contrôle affectée à cette commande. Par exemple, «A» affecte cette commande à Ctrl + Maj + A. Cet argument est facultatif et est utilisé uniquement pour les commandes.
  
_pxHelpTopic_ (**xltypeStr**)
  
Référence facultative au fichier d'aide (. chm ou. hlp) à afficher lorsque l'utilisateur clique sur le bouton aide (lorsque votre fonction personnalisée est affichée). Peut être sous la forme `filepath!HelpContextID` ou `https://address/path_to_file_in_site!0`. Les deux parties avant et après le «!» sont obligatoires.  *HelpContextID* ne doit pas contenir de guillemets simples et sera converti par Excel en entier non signé de 4 octets de long, sous forme décimale. Lorsque vous utilisez le formulaire d'URL, Excel ouvre uniquement le fichier d'aide référencé. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Chaîne facultative qui décrit votre fonction personnalisée lorsque celle-ci est sélectionnée dans l'Assistant fonction.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Facultatif. La première des chaînes qui décrivent les arguments personnalisés de la fonction lorsque la fonction est sélectionnée dans l'Assistant fonction. Dans Excel 2003 et versions antérieures, **xlfRegister** peut prendre, au plus, 30 arguments afin que vous puissiez fournir cette aide pour les 20 premiers de vos arguments de fonction uniquement. À partir d'Excel 2007, **xlfRegister** peut prendre jusqu'à 255 arguments afin que vous puissiez fournir cette aide pour un maximum de 245 paramètres de fonction. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si l'inscription a réussi, cette fonction renvoie l'ID de registre de la fonction (**xltypeNum**), qui peut être utilisé dans les appels à **xlUDF** et **xlfUnregister** dans une dll, ou avec **Call** et Unregister dans une feuille macro XLM. **** Dans le cas contraire, elle renvoie une #VALUE! «. 
  
## <a name="remarks"></a>Remarques

### <a name="data-types"></a>Types de données

L'argument _pxTypeText_ spécifie le type de données de la valeur renvoyée et les types de données de tous les arguments de la fonction ou de la ressource de code de la dll. Le premier caractère de _pxTypeText_ spécifie le type de données de la valeur de retour. Les autres caractères indiquent les types de données de tous les arguments. Par exemple, une fonction DLL qui renvoie un nombre à virgule flottante et prend un nombre entier et un nombre à virgule flottante comme arguments exigerait «BIB» pour l'argument _pxTypeText_ . 
  
Les types de données et les structures utilisés par Excel pour échanger des données avec des XLL sont résumées dans les deux tableaux suivants.
  
Le premier tableau répertorie les types pris en charge dans toutes les versions d'Excel.
  
|**Type de données**|**Passer par valeur**|**Passer par référence (pointeur)**|**Comments**|
|:-----|:-----|:-----|:-----|
|Booléen  <br/> |A  <br/> |L  <br/> |short [entier] (0 = false ou 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |Chaîne d’octets ASCII se terminant par null  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Chaîne d'octets ASCII comptés  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||MOT 16 bits  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |entier signé 16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |entier signé 32 bits  <br/> |
|FP  <br/> ||K  <br/> |Structure de tableau à virgule flottante  <br/> |
|Tableau  <br/> ||O  <br/> |Trois arguments sont passés:<br/>-unsigned short int\*<br/>-unsigned short int\*<br/>-double []  <br/> |
|XLOPER  <br/> ||P  <br/> |Tableaux et valeurs de feuille de calcul de type variable  <br/> |
|||R  <br/> |Valeurs, tableaux et références de plage  <br/> |
   
Dans Excel 2007, les types de données suivants ont été introduits pour prendre en charge les grandes grilles et les longues chaînes Unicode.
  
|**Type de données**|**Passer par valeur**|**Passer par référence (pointeur)**|**Comments**|
|:-----|:-----|:-----|:-----|
|Short non signé\*  <br/> ||C%, F%  <br/> |Chaîne de caractères larges Unicode terminée par un caractère null  <br/> |
|Short non signé\*  <br/> ||D%, G%  <br/> |Chaîne Unicode à caractères larges comptés  <br/> |
|FP12  <br/> ||K%  <br/> |Structure de tableau à virgule flottante à grande grille  <br/> |
|Tableau  <br/> ||O%  <br/> |Trois arguments sont passés:<br/>-signé int \* /RW\*<br/>-signe int \* /col signé\*<br/>-double []  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Tableaux et valeurs de feuille de calcul de type variable  <br/> |
|||U  <br/> |Valeurs, tableaux et références de plage  <br/> |
   
À partir d'Excel 2010, les types de données suivants ont été introduits:
  
|**Type de données**|**Passer par valeur**|**Passer par référence (pointeur)**|**Comments**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X  <br/> |Le handle asynchrone est utilisé pour suivre un appel de fonction asynchrone en attente par Excel et le XLL. L'existence du type de paramètre dans la chaîne de type désigne également la fonction comme étant asynchrone. Pour plus d'informations sur les fonctions asynchrones, consultez la rubrique [fonctions asynchrones définies par l'utilisateur](asynchronous-user-defined-functions.md).  <br/> |
   
Les types de chaînes**F**, **F%**, **G** et **G%** sont utilisés pour les arguments qui sont modifiés directement (modified-in-place). 
  
Lorsque vous utilisez les types de données affichés dans le tableau précédent, gardez à l'esprit les points suivants:
  
- Les déclarations en langage C partent du principe que votre compilateur utilise des doubles de 8 octets, des nombres entiers courts de 2 octets et des entiers longs de 4 octets par défaut.
    
- Toutes les fonctions dans les dll et les ressources de code sont appelées à l'aide de la Convention d'appel **_ _ stdcall** . 
    
- Toute fonction qui renvoie un type de données par référence, c'est-à-dire qui renvoie un pointeur vers un autre, peut retourner en toute sécurité un pointeur null. Excel interprète un pointeur null comme un #NUM! «.
    
## <a name="additional-data-type-information"></a>Informations supplémentaires sur le type de données

Cette section contient des informations détaillées sur les types de données **E**, **f**, **f%**, **g**, **g%**, **K**, **O**, **P**, **Q**, **R**et **U** , ainsi que d'autres informations sur le _pxTypeText _argument. 
  
### <a name="e-data-type"></a>E, type de données

Excel s'attend à ce qu'une DLL utilisant le type de données E passe des pointeurs vers des nombres à virgule flottante sur la pile. Cela peut entraîner des problèmes avec certains langages (par exemple, Borland C++) qui s'attendent à ce que le numéro soit passé sur la pile de l'émulateur du coprocesseur. La solution de contournement consiste à transmettre un pointeur vers le numéro sur la pile de coprocesseur. L'exemple suivant montre comment retourner un double à partir de Borland C++.
  
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

Avec les types de données **f**, **f%**, **g**et **g%** , une fonction peut modifier une mémoire tampon de chaîne allouée par Excel. Si le code de type de la valeur renvoyée est l'un de ces types, Excel ignore la valeur renvoyée par la fonction. Au lieu de cela, Excel recherche dans la liste des arguments de fonction le premier type de données correspondant (**f**, **f%**, **g**ou **g%**), puis prend le contenu actuel de la mémoire tampon de chaîne allouée en tant que valeur de retour. Toutes les versions d'Excel allouent 256 octets pour les chaînes **F** et **G** ASCII, et en commençant dans Excel 2007 65 536 les octets sont alloués, soit suffisant pour 32 768 caractères Unicode, pour les chaînes Unicode **f%** et **G%** . N'oubliez pas que les mémoires tampon doivent inclure un nombre de caractères (types **g** et **g%**) ou un caractère d'arrêt nul (types **f** et **f%**), afin que les longueurs maximales de chaîne soient 255 et 32 767. Les chaînes Unicode et, par conséquent, les arguments **F%** et **G%** sont disponibles uniquement par le biais de l'API C dans Excel. 
  
### <a name="k-and-k-data-types"></a>Types de données K et K%

Les types de données **k** et **k%** utilisent des pointeurs vers les structures FP et FP12 de taille variable, respectivement. Ces structures sont définies dans XLLCALL. H. Les structures FP12, et par conséquent tapez **K%** arguments, sont uniquement prises en charge à partir d'Excel 2007. 
  
### <a name="o-and-o-data-types"></a>Types de données O et O%

Les types de données **o** et **o%** ne peuvent être utilisés que pour les arguments, pas les valeurs renvoyées, bien que les valeurs puissent être renvoyées après la modification d'un argument de type **o** ou **o%** . Chacun passe trois éléments: un pointeur vers le nombre de lignes dans une matrice, un pointeur vers le nombre de colonnes dans un tableau et un pointeur vers un tableau à deux dimensions de nombres à virgule flottante. 
  
Pour modifier un tableau passé par le type de données O ou O% sur place, vous pouvez utiliser «>O» ou «>O%» comme argument _pxTypeText_ . Pour plus d'informations sur la modification d'un tableau, reportez-vous à la section «modification en place: fonctions déclarées void» de cette rubrique. 
  
Le type de données **O** a été créé pour des fins de compatibilité directe avec les dll Fortran, qui passent des arguments par référence. 
  
Le **O%** est pris en charge à partir d'Excel 2007 et s'ajuste au plus grand nombre de lignes prises en charge par Excel. 
  
### <a name="p-and-q-data-types"></a>Types de données P et Q

Lorsque les arguments de la fonction DLL sont enregistrés comme prenant en charge le type **P** XLOPER ou le type **Q** XLOPER12, Excel convertit des références à cellule unique en valeurs simples et des références à plusieurs cellules en tableaux lors de la préparation de ces arguments. En d'autres termes, les types **P** et **Q** arriveront toujours dans votre fonction comme l'un des types suivants: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**ou **xltypeNil **, mais pas **XltypeRef** ou **xltypeSRef** , car ils sont toujours déréférencés. Les objets **XLOPER12**et, par conséquent, les arguments **Q** , sont pris en charge uniquement à partir d'Excel 2007. 
  
Si les types **xltypeMissing** ou **xltypeNil** sont utilisés pour les valeurs de retour, elles sont interprétées par Excel comme une valeur numérique zéro. **xltypeMissing** est transmis lorsque l'appelant omet un argument. **xltypeNil** est transmis lorsque l'appelant transmet une référence à une cellule vide. Lorsqu'une plage de cellules est convertie en **xltypeMulti** pour être transmise en tant que type **P** ou **Q**, toutes les cellules vides comprises dans la plage sont converties en éléments de tableau **xltypeNil** . Les éléments manquants dans un tableau littéral sont passés de la même manière que les éléments **xltypeNil** . 
  
### <a name="volatile-functions-and-recalculation"></a>Fonctions volatiles et recalcul

Dans une feuille de calcul, vous pouvez créer une ressource de code ou une fonction DLL volatile, afin qu'elle recalcule chaque fois que la feuille de calcul recalcule. Pour ce faire, ajoutez un point d'exclamation (!) après le dernier code d'argument de l'argument _pxTypeText_ . 
  
> [!NOTE]
> Par défaut, les fonctions qui prennent type **R** XLOPER ou type **U** XLOPER12 et qui sont inscrites en tant qu'équivalents **#** de feuille macro (type; consultez la section suivante) sont gérées comme volatile dans Excel. 
  
### <a name="functions-declared-as-void"></a>Fonctions déclarées void

Il existe deux cas qui appellent la déclaration d'une fonction comme renvoyant void. Dans les deux cas, la fonction renvoie son résultat par d'autres moyens.
  
#### <a name="modifying-in-place"></a>Modification sur place

Vous pouvez utiliser un seul chiffre _n_ pour le code de type de retour dans _pxTypeText_, où _n_ est un nombre compris entre 1 et 9. Cela indique à Excel d'utiliser la valeur de la variable à l'emplacement désigné par l'argument _n_th dans _pxTypeText_ en tant que valeur de retour. Cette fonctionnalité est également appelée modification sur place. L'argument _n_th doit être un type de données de transfert par référence (C, D, E, F, F%, G, G%, K, K%, L, M, N, O, O%, P, Q, R ou U). La fonction DLL ou la ressource de code doit également être déclarée à l'aide du mot clé **void** dans les langages C/C++ (ou le mot clé de **procédure** en langage Pascal). 
  
Par exemple, une fonction DLL qui prend une chaîne terminée par un caractère null et deux pointeurs vers des entiers comme arguments peut modifier la chaîne sur place. Utilisez «1FMM» comme argument _pxTypeText_ et déclarez la fonction comme void. 
  
Les versions précédentes d'Excel **\>** utilisaient au début de _pxTypeText_ pour indiquer que la fonction a été déclarée comme void et que le premier argument devait être modifié sur place, il n'était pas possible de modifier un argument autre que le premier. Équivaut **\>** à _n_ = 1 dans les versions actuelles d'Excel et cette utilisation de **\>** dans les fonctions synchrones est prise en charge uniquement à des fins de compatibilité descendante. 
  
#### <a name="asynchronous-functions"></a>Fonctions asynchrones

Une fonction asynchrone, dénotée à l'aide d'un paramètre de type X dans **pxTypeText**, ne renvoie pas son résultat à partir de l'appel de la fonction initiale. Au lieu de cela, vous devez déclarer une fonction asynchrone comme void et, par la suite, le complément renvoie le résultat via un rappel. La fonction asynchrone doit être inscrite en **\>** utilisant au début de **pxTypeText**. Dans les fonctions asynchrones, **\>** indique que la fonction est déclarée void, mais n'indique pas que le premier argument est modifié sur place. Pour plus d'informations sur les fonctions asynchrones, consultez la rubrique [fonctions asynchrones définies par l'utilisateur](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Enregistrement des fonctions de feuille de calcul en tant qu'équivalents de feuille macro (gestion des cellules non calculées)

Le fait **#** de placer un caractère après le dernier code de paramètre dans _pxTypeText_ donne aux fonctions les mêmes autorisations d'appel que les fonctions d'une feuille macro. Elle comprennent notamment : 
  
- La fonction peut récupérer les valeurs des cellules qui n'ont pas encore été calculées dans ce cycle de recalcul.
    
- La fonction peut appeler n'importe laquelle des informations XLM (classe 2), par exemple **xlfGetCell**.
    
- Si le signe dièse (#) n'est pas présent: l'évaluation d'une cellule non calculée génère une erreur **xlretUncalced** et la fonction active est rappelée une fois que la cellule a été calculée; l'appel d'une fonction d'informations XLM autre que **xlfCaller** génère une erreur **xlretInvXlfn** . 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Enregistrement des fonctions de feuille de calcul en tant que thread-safe

À partir d'Excel 2007, Excel peut effectuer un recalcul de classeurs multithreads. Cela signifie qu'il peut affecter différentes instances d'une fonction thread-safe aux threads simultanés pour la réévaluation. À partir d'Excel 2007, la plupart des fonctions de feuille de calcul intégrées sont thread-safe. À partir d'Excel 2007, Excel autorise également les XLL à enregistrer des fonctions de feuille de calcul en tant que thread-safe. Pour ce faire, incluez **$** un caractère après le dernier code de paramètre dans _pxTypeText_. 
  
> [!NOTE]
> Seules les fonctions de feuille de calcul peuvent être déclarées comme thread-safe. Excel ne considère pas une fonction équivalente de feuille macro comme étant thread-safe, de sorte que vous **#** ne **$** pouvez pas ajouter les deux et les caractères à l'argument _pxTypeText_ . 
  
Si vous avez inscrit une fonction thread-safe, vous devez vous assurer qu'elle se comporte de manière thread-safe, bien qu'Excel rejette tous les appels non sécurisés de thread via l'API C. Par exemple, si une fonction thread-safe tente d'appeler **xlfGetCell**, l'appel échoue avec l'erreur **xlretNotThreadSafe** . 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Enregistrement des fonctions de feuille de calcul en tant que cluster-safe

À partir d'Excel 2010, Excel peut décharger les appels de fonction vers un fournisseur de cluster de calcul désigné. Pour plus d'informations, consultez la rubrique [fonctions de sécurité](cluster-safe-functions.md)des clusters. Toutes les fonctions de feuille de calcul XLL enregistrées en tant que cluster-safe prennent part au déchargement si un cluster est disponible. Les fonctions de cluster sont inscrites en incluant **&amp;** le caractère qui suit le dernier code de paramètre dans l'argument _pxTypeText_ . 
  
Si vous avez inscrit une fonction comme étant sécurisée en clusters, vous devez vous assurer qu'elle se comporte de manière sécurisée en cluster. Pour plus d'informations, consultez la rubrique [fonctions de sécurité](cluster-safe-functions.md)des clusters.
  
> [!NOTE]
> Seules les fonctions de feuille de calcul peuvent être déclarées comme étant sécurisées pour les clusters. Excel ne considère pas une fonction équivalente de feuille macro comme étant sécurisée pour les clusters, de **#** sorte **&amp;** que vous ne pouvez pas ajouter les deux et les caractères à l'argument _pxTypeText_ . Les fonctions de feuille de calcul peuvent être déclarées en tant que thread-safe et thread-safe. Dans ce cas, Excel permet à ces fonctions de prendre part au recalcul multithread lorsque le déchargement du cluster est désactivé. 
  
### <a name="category-names"></a>Noms de catégorie

Utilisez les instructions suivantes pour déterminer la catégorie dans laquelle placer vos fonctions XLL.
  
- Si la fonction effectue une opération qui pourrait être réalisée par l'utilisateur dans le cadre de l'interface utilisateur de votre complément, vous devez placer la fonction dans la catégorie **commandes** . 
    
- Si la fonction renvoie des informations sur l'état du complément ou toute autre information utile, vous devez placer la fonction dans la catégorie d' **informations** . 
    
- Un complément ne doit jamais ajouter de fonctions ni de commandes à la catégorie **définie par l'utilisateur** . Cette catégorie est destinée à l'usage exclusif des utilisateurs finals. 
    
La catégorie est spécifiée à l'aide du paramètre _pxCategory_ sur **xlfRegister**. Il peut s'agir d'un nombre ou d'un texte correspondant à l'une des catégories standard codées en dur ou du texte d'une nouvelle catégorie spécifiée par la DLL. Si le texte indiqué n'existe pas déjà, Excel crée une nouvelle catégorie portant ce nom.
  
Le tableau suivant répertorie les catégories standard qui sont visibles lorsque vous affichez la boîte de dialogue **coller une fonction** à partir d'une feuille de calcul. 
  
|**Number**|**Text**|
|:-----|:-----|
|0,1  <br/> |Financier  <br/> |
|n°2  <br/> |Date &amp; et heure  <br/> |
|3  <br/> |Math &amp; Trig  <br/> |
|4  <br/> |Texte  <br/> |
|disque  <br/> |Logique  <br/> |
|6.x  <br/> |Lookup &amp; Reference  <br/> |
|7j/7  <br/> |Database  <br/> |
|8bits  <br/> |Statistiques  <br/> |
|4,9  <br/> |Informations  <br/> |
|13  <br/> |Personnalisées  <br/> |
||Ingénierie (en commençant dans Excel 2007)  <br/> |
||Cube (en commençant dans Excel 2007)  <br/> |
   
En outre, ces catégories sont également visibles lorsque vous affichez la boîte de dialogue **coller une fonction** à partir d'une feuille macro. 
  
|**Number**|**Text**|
|:-----|:-----|
|10  <br/> |Commandes  <br/> |
|a4  <br/> |DDE/Externe  <br/> |
|an  <br/> |Personnalisation  <br/> |
|kg  <br/> |Contrôle de macros  <br/> |
   
### <a name="example"></a>Exemple

Voir le code de la fonction **xlAutoOpen** dans `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Voir aussi

- [REGISTER.ID](xlfregisterid.md)
- [ANNULER l'inscription](xlfunregister-form-1.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

