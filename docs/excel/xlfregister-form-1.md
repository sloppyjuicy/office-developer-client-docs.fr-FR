---
title: xlfRegister (formulaire 1)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- fonction xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: c730124c-1886-4a0f-8f06-79763025537d
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3cd2e5072c8602fe301028e69592220a8345c211
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385080"
---
# <a name="xlfregister-form-1"></a>xlfRegister (formulaire 1)

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d’une commande DLL ou XLL lui-même a été appelée par Microsoft Excel. Cela est égale à l’appel de **Registre** à partir d’une feuille de macro Excel XLM. 
  
**xlfRegister** peut être appelée sous deux formes : 
  
- xlfRegister (formulaire 1) : enregistre une seule commande ou une fonction.
    
- [xlfRegister (formulaire 2)](xlfregister-form-2.md): charges et Active une solution XLL.
    
Appelé dans le formulaire 1, cette fonction propose une fonction DLL ou la commande pour Excel, définit son compteur d’utilisation à 1 et renvoie son ID d’enregistrement, qui peut être utilisé pour appeler la fonction ultérieurement à l’aide de la [xlUDF](xludf.md) ou la fonction **xlfCall** . L’ID de l’enregistrement est également utilisé pour annuler l’inscription de la fonction à l’aide de [xlfUnregister (formulaire 1)](xlfunregister-form-1.md). Si la fonction a été enregistrée, rappeler **xlfRegister** incrémente son compteur d’utilisation. 
  
Cette forme de la fonction définit également le nom masqué qui est l’argument texte fonction, _pxFunctionText_, et qui correspond à l’ID de l’enregistrement de la fonction ou la commande. Lorsque vous annulez l’inscription de la fonction, supprimez ce nom en utilisant la [xlfSetName](xlfsetname.md). Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).
  
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
  
Le nom de la DLL qui contient la fonction. Cela peut être obtenu en appelant la fonction XLL seule [xlGetName](xlgetname.md) si la fonction inscrite est également dans la DLL en cours d’exécution. 
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
Si une chaîne, le nom de la fonction à appeler telle qu’elle apparaît dans le code de la DLL. Si un nombre, la propriété ordinal exporter nombre de la fonction à appeler. Pour plus de clarté, utilisez toujours la forme de chaîne.
  
_pxTypeText_ (**xltypeStr**)
  
Chaîne facultative qui spécifie les types d’arguments de la fonction et le type de la valeur de retour de la fonction. Pour plus d’informations, voir la section Remarques. Cet argument peut être omis pour une autonome DLL (XLL) qui inclut une [fonction xlAutoRegister](xlautoregister-xlautoregister12.md) ou le **xlAutoRegister12**. 
  
> [!NOTE]
> **xlAutoRegister12** est uniquement pris en charge dans Excel 2007. 
  
Si **xlfRegister** est appelé avec cet argument manquant, Excel appelle **xlAutoRegister** ou **xlAutoRegister12**, si existe dans la DLL spécifiée, qui doit enregistrer puis correctement la fonction en fournissant les informations.
  
_pxFunctionText_ (**xltypeStr**)
  
Le nom de la fonction tel qu’il apparaîtra dans l’Assistant fonction. Cet argument est facultatif ; s’il est omis, la fonction n’est pas disponible dans l’Assistant fonction et peut être appelée uniquement à l’aide de la fonction **d’appel** à l’aide de l’ID de l’enregistrement de fonctions à partir d’une feuille de macro XLM. Par conséquent, pour une utilisation ordinaire de feuille de calcul, vous devez gérer cet argument selon les besoins. 
  
_pxArgumentText_ (**xltypeStr**)
  
Une chaîne de texte facultative qui décrit les arguments de la fonction. L’utilisateur voit ce dans l’Assistant fonction. S’il est omis, Excel construit descriptions de base à partir de _pxTypeText_.
  
_pxMacroType_ (**xltypeNum** ou **xltypeInt**)
  
Un argument facultatif qui indique le type d’entrée XLL point. La valeur par défaut, s’il est omis, est 1.
  
|||||
|:-----|:-----|:-----|:-----|
| _valeur pxMacroType_ <br/> |0  <br/> |1  <br/> |2  <br/> |
|Peut être appelée à partir d’une feuille de calcul  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Peut être appelée à partir d’une feuille macro  <br/> |Oui  <br/> |Oui  <br/> |Oui  <br/> |
|Peut être appelée à partir d’une définition de nom défini  <br/> |Oui  <br/> |Oui  <br/> |Oui  <br/> |
|Peut être appelée à partir d’une expression de mise en forme conditionnelle  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Dans l’Assistant fonction pour les fonctions de feuille de calcul  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Dans l’Assistant fonction pour les fonctions de feuille macro  <br/> |Non  <br/> |Oui  <br/> |Oui  <br/> |
   
En pratique, vous devez utiliser 1 pour les fonctions de feuille de calcul, 1 pour les fonctions équivalent de feuille macro (enregistré en tant que type **#**) que vous souhaitez appeler à partir de la feuille de calcul et 2 pour les commandes. 
  
> [!NOTE]
> Commandes XLL sont masquées et n’affiche pas dans les boîtes de dialogue pour l’exécution de macros, bien que leurs noms peuvent être n’importe où entrés un nom de commande valide est requis. 
  
_pxCategory_ (**xltypeStr** ou **xltypeNum**)
  
Un argument facultatif qui vous permet de spécifier quelle catégorie de la nouvelle fonction ou la commande doit appartenir. L’Assistant fonction divise les fonctions par type (catégorie). Vous pouvez spécifier un nom de catégorie ou d’un numéro séquentiel, où le nombre est l’emplacement dans lequel la catégorie apparaît dans l’Assistant fonction. Pour plus d’informations, voir la section « Noms de catégorie ». S’il est omis, la catégorie définie par l’utilisateur est supposée.
  
_pxShortcutText_ (**xltypeStr**)
  
Une chaîne de caractères, la casse qui indique la touche attribuée à cette commande. Par exemple, « A » affecte cette commande à CTRL + MAJ + A. Cet argument est facultatif et est utilisé pour les commandes uniquement.
  
_pxHelpTopic_ (**xltypeStr**)
  
Une référence facultative pour le fichier d’aide (.hlp ou .chm) à afficher lorsque l’utilisateur clique sur le bouton Aide (lorsque votre fonction personnalisée est affichée). Peut être sous la forme `filepath!HelpContextID` ou `https://address/path_to_file_in_site!0`. Les deux composants avant et après le « ! » sont requis.  *HelpContextID* ne doit pas comporter de guillemets simples et seront convertis par Excel à un entier non signé de 4 octets, au format décimal. Lorsque vous utilisez la forme d’URL, Excel ouvre uniquement le fichier d’aide référencé. 
  
_pxFunctionHelp_ (**xltypeStr**)
  
Chaîne facultative qui décrit votre fonction personnalisée lorsqu’elle est sélectionnée dans l’Assistant fonction.
  
_pxArgumentHelp1_ (**xltypeStr**)
  
Facultatif. La première des chaînes qui décrivent les arguments de la fonction personnalisées lorsque la fonction est sélectionnée dans l’Assistant fonction. Dans Excel 2003 et versions antérieures, **xlfRegister** peut prendre, au maximum, 30 arguments afin que vous pouvez fournir cette aide pour les 20 premiers votre d’arguments de fonction uniquement. À compter d’Excel 2007, **xlfRegister** peut prendre jusqu'à 255 arguments afin que vous pouvez fournir cette aide pour les paramètres de la fonction 245 jusqu'à. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si l’inscription a réussi, cette fonction renvoie l’identificateur de Registre de la fonction (**xltypeNum**), qui peut être utilisée dans les appels à **xlUDF** et **xlfUnregister** dans une DLL ou avec des **appels** et **Annuler l’inscription** dans une feuille de macro XLM. Sinon, elle renvoie une #VALUE ! erreur. 
  
## <a name="remarks"></a>Remarques

### <a name="data-types"></a>Types de données

L’argument _pxTypeText_ Spécifie le type de données de la valeur de retour et les types de données de tous les arguments de la ressource du code ou de la fonction DLL. Le premier caractère de _pxTypeText_ Spécifie le type de données de la valeur de retour. Les caractères suivants indiquent les types de données de tous les arguments. Par exemple, une fonction DLL qui renvoie un nombre à virgule flottante et qui prend un entier et un nombre à virgule flottante comme arguments obligerait « SALOPETTES » pour l’argument _pxTypeText_ . 
  
Les types de données et les structures utilisées par Excel pour échanger des données avec les XLL sont récapitulées dans les deux tables suivantes.
  
Le premier tableau répertorie les types pris en charge dans toutes les versions d’Excel.
  
|**Type de données**|**Passer par valeur**|**Passer par référence (pointeur)**|**Comments**|
|:-----|:-----|:-----|:-----|
|Boolean  <br/> |A  <br/> |L  <br/> |abréviation [int] (0 = false ou 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|Char\*  <br/> ||C, F  <br/> |Chaîne d’octets ASCII terminée  <br/> |
|char non signé\*  <br/> ||D, G  <br/> |Chaîne d’octets ASCII compté  <br/> |
|court non signé [int]  <br/> |H  <br/> ||MOT de 16 bits  <br/> |
|abréviation [signée] [int]  <br/> |I  <br/> |M  <br/> |nombre entier signé de 16 bits  <br/> |
|[signé long] int  <br/> |J  <br/> |N  <br/> |nombre entier signé de 32 bits  <br/> |
|FP  <br/> ||K  <br/> |Structure de tableau à virgule flottante  <br/> |
|Tableau  <br/> ||O  <br/> |Trois arguments sont transférés :<br/>-entier court\*<br/>-entier court\*<br/>-double]  <br/> |
|XLOPER  <br/> ||P  <br/> |Les tableaux et les valeurs de variable de type feuille de calcul  <br/> |
|||R  <br/> |Valeurs, des tableaux et des références de plage  <br/> |
   
Dans Excel 2007, que les types de données suivants ont été introduits pour prendre en charge les grilles plus grandes long Unicode des chaînes.
  
|**Type de données**|**Passer par valeur**|**Passer par référence (pointeur)**|**Comments**|
|:-----|:-----|:-----|:-----|
|court non signé\*  <br/> ||C, F %  <br/> |Chaîne à caractère élargi Unicode terminée par null  <br/> |
|court non signé\*  <br/> ||% D, G  <br/> |Chaîne de caractères étendus compté Unicode  <br/> |
|FP12  <br/> ||K %  <br/> |Structure de tableau à virgule flottante plus grande grille  <br/> |
|Tableau  <br/> ||O %  <br/> |Trois arguments sont transférés :<br/>-signé int \* / RW\*<br/>-signé int \* / COL\*<br/>-double]  <br/> |
|XLOPER12  <br/> ||Q  <br/> |Les tableaux et les valeurs de variable de type feuille de calcul  <br/> |
|||U  <br/> |Valeurs, des tableaux et des références de plage  <br/> |
   
Types de démarrage dans Excel 2010, les données suivantes ont été apportées :
  
|**Type de données**|**Passer par valeur**|**Passer par référence (pointeur)**|**Comments**|
|:-----|:-----|:-----|:-----|
|XLOPER12  <br/> ||X   <br/> |La poignée asynchrone est utilisée pour effectuer le suivi d’un appel de fonction asynchrone en attente par Excel et de la ressource XLL. L’existence du type de paramètre dans la chaîne de type désigne également la fonction comme asynchrone. Pour plus d’informations sur des fonctions asynchrones, voir [Fonctions Asynchronous User-Defined](asynchronous-user-defined-functions.md).  <br/> |
   
Les types de chaînes **F**, **% F**, **G**et **G %** sont utilisés pour les arguments qui sont modifiées en place. 
  
Lorsque vous travaillez avec les types de données affichées dans le tableau précédent, prenez en compte les éléments suivants :
  
- Les déclarations en langage C supposent que votre compilateur utilise 8 octets doubles, entiers courts de 2 octets et entiers longs de 4 octets par défaut.
    
- Toutes les fonctions dans les DLL et les ressources de code sont appelées à l’aide de la convention d’appel **__stdcall** . 
    
- Une fonction qui renvoie un type de données par référence, autrement dit, qui retourne un pointeur vers un élément, peut renvoyer en toute sécurité un pointeur null. Excel interprète un pointeur null comme un #NUM ! erreur.
    
## <a name="additional-data-type-information"></a>Type de données supplémentaires

Cette section contient des informations détaillées sur les **E**, **F**, **F %**, **G**, **G %**, **K**, **O**, **P**, **Q**, **R**et **U** des types de données et autres informations sur la pxTypeText _ _argument. 
  
### <a name="e-data-type"></a>Type de données E

Excel attend une DLL à l’aide du type de données E pour transmettre des pointeurs aux nombres à virgule flottante sur la pile. Cela peut entraîner des problèmes avec certaines langues (par exemple, Borland C++) que vous pensez que le nombre à transmettre à la pile d’émulateur coprocesseur. La solution de contournement consiste à passer un pointeur vers le numéro de la pile coprocesseur. L’exemple suivant montre comment renvoyer une valeur double à partir de C++ Borland.
  
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

### <a name="f-f-g-and-g-data-types"></a>% F, F, G et G % des types de données

**F**, **F %**, **G**, et les types de données **G %** , une fonction peut modifier un tampon de chaîne qui est alloué par Excel. Si le code de type de valeur de retour est un de ces types, Excel ignore la valeur renvoyée par la fonction. Au lieu de cela, Excel recherche dans la liste d’arguments de la fonction pour le premier type de données correspondant (**F**, **F %**, **G**ou **G %**) et effectue le contenu actuel de la mémoire tampon de chaîne allouée comme valeur de retour. Toutes les versions d’Excel allouent plus de 256 octets **F** et **G** des chaînes ASCII, et à compter d’Excel, 2007 65 536 octets sont allouées, suffisamment de 32 768 caractères Unicode, **F %** et **% G** des chaînes Unicode. N’oubliez pas que les mémoires tampon doivent inclure un caractère count (types **G** et **G %**) ou un caractère null (types **F** et **F %**), afin que la longueur maximale des chaînes est 255 et 32 767. Les chaînes Unicode et par conséquent type **F** et **G %** arguments, sont disponibles uniquement par le biais de l’API C dans Excel. 
  
### <a name="k-and-k-data-types"></a>K et types de données K %

Les types de données **K** et **K %** utilisent respectivement des pointeurs vers les structures FP et FP12 taille variable. Ces structures sont définies dans XLLCALL. H. Structures FP12 et par conséquent **K %** des arguments de type, sont uniquement en charge à compter d’Excel 2007. 
  
### <a name="o-and-o-data-types"></a>O et types de données O %

Les types de données **O** et **O %** peuvent uniquement être utilisés pour les arguments, ne retournent pas de valeurs, bien que les valeurs peuvent être renvoyées mon la modification d’un argument de type **O** ou **O %** en place. Chaque passe trois éléments : un pointeur vers le nombre de lignes dans un tableau, un pointeur vers le nombre de colonnes dans un tableau et un pointeur vers un tableau à deux dimensions de nombres à virgule flottante. 
  
Pour modifier un tableau passé par O ou O des types de données % en place, vous pouvez utiliser « > O » ou « > O % » en tant qu’argument _pxTypeText_ . Pour plus d’informations sur la modification d’un tableau, consultez la section « Modification en Place : fonctions déclarées Void » dans cette rubrique. 
  
Le type de données **O** a été créé pour la compatibilité directe avec les DLL Fortran, qui transfèrent les arguments par référence. 
  
Le **O %** est pris en charge dans Excel 2007 et prend en charge le plus grand nombre de lignes qui prend en charge par Excel. 
  
### <a name="p-and-q-data-types"></a>Types de données P et Q

Lorsque arguments de la fonction DLL sont inscrits comme prenant type **P** XLOPER ou tapez XLOPER12s **Q** , Excel convertit les références de cellule unique à valeurs simples et les références de cellules à des tableaux lors de la préparation de ces arguments. En d’autres termes, les types **P** et **Q** arrive toujours dans la fonction en tant qu’un de ces types : xltypeNil **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**ou ** **, mais pas **xltypeRef** ou **xltypeSRef** , car elles sont toujours suppression. S **XLOPER12**et, par conséquent, les arguments de type **Q** , sont uniquement en charge à compter d’Excel 2007. 
  
Si les types **xltypeMissing** ou **xltypeNil** est utilisées pour les valeurs de retour, elles sont interprétées par Excel comme numérique zéro. **xltypeMissing** est transmis lorsque l’appelant omet un argument. **xltypeNil** est transmis lorsque l’appelant transmet une référence à une cellule vide. Lorsqu’une plage de cellules est convertie en une **xltypeMulti** à transmettre en tant que type **P** ou **Q**, toutes les cellules vides dans la plage sont convertis en éléments de tableau **xltypeNil** . Les éléments manquants dans un littéral de tableau sont de même transmis en tant qu’éléments **xltypeNil** . 
  
### <a name="volatile-functions-and-recalculation"></a>Fonctions volatiles et recalcul

Une feuille de calcul, peut avoir une ressource du code ou de la fonction DLL volatiles, afin qu’il recalcule chaque recalcul de la feuille de calcul. Pour ce faire, ajoutez un point d’exclamation ( !) après le dernier code argument dans l’argument _pxTypeText_ . 
  
> [!NOTE]
> Par défaut, les fonctions qui acceptent type XLOPER **R** ou tapez XLOPER12s **U** et qui sont inscrits en tant que macro feuille équivalents (type **#**; voir la section suivante) sont traitées comme volatiles dans Excel. 
  
### <a name="functions-declared-as-void"></a>Fonctions déclarées void comme

Il existe deux cas d’appel de la déclaration d’une fonction comme renvoyant des valeurs nulles. Dans les deux cas, la fonction retourne son résultat par d’autres moyens.
  
#### <a name="modifying-in-place"></a>Modification sur place

Vous pouvez utiliser un seul chiffre _n_ pour le code de type de retour dans _pxTypeText_, où _n_ est un nombre compris entre 1 et 9. Ceci indique à Excel à prendre la valeur de la variable à l’emplacement désigné par l’argument _n_th dans _pxTypeText_ comme valeur de retour. Il est également appelé modification sur place. L’argument _n_th doit être de type de données passe par référence (C, D, E, F, F %, G, G %, K, K %, L, M, N, O, O %, P, Q, R ou U). La ressource du code ou de la fonction DLL doit également être déclarée avec le mot clé **void** dans les langages C/C++ (ou le mot clé **procédure** en langage Pascal). 
  
Par exemple, une fonction DLL qui accepte une chaîne de caractère nul et deux pointeurs à utiliser des entiers comme arguments peut modifier la chaîne en place. Utilisez « 1FMM » en tant qu’argument _pxTypeText_ et déclarer la fonction comme void. 
  
Les versions antérieures d’Excel utilisé **\>** au début de _pxTypeText_ pour indiquer que la fonction est déclarée comme void et que le premier argument était à modifier en place, il n’a aucun moyen de modifier un argument autre que le premier. Le **\>** équivaut à _n_ = 1 dans les versions d’Excel en cours et utilisation de **\>** dans les fonctions synchrones est pris en charge pour la compatibilité descendante uniquement. 
  
#### <a name="asynchronous-functions"></a>Fonctions asynchrones

Une fonction asynchrone, indiquée à l’aide d’un paramètre de type X dans **pxTypeText**, ne retourne pas son résultat à partir de l’appel de fonction initiale. Au lieu de cela, vous devez déclarer une fonction asynchrone comme void et version ultérieure, le complément renvoie le résultat via un rappel. La fonction asynchrone doit être enregistrée à l’aide de **\>** au début de **pxTypeText**. Dans des fonctions asynchrones, **\>** indique que la fonction est déclarée comme void, mais n’indique pas que le premier argument est modifié en place. Pour plus d’informations sur des fonctions asynchrones, voir [Fonctions Asynchronous User-Defined](asynchronous-user-defined-functions.md). 

### <a name="registering-worksheet-functions-as-macro-sheet-equivalents-handling-uncalculated-cells"></a>Inscription des fonctions de feuille de calcul en tant qu’équivalents de feuille macro (gestion des cellules non calculées)

Placer un **#** caractère après le code du paramètre dernière dans _pxTypeText_ donne la fonction appel mêmes autorisations que les fonctions d’une feuille macro. Celles-ci sont les suivantes : 
  
- La fonction peut récupérer les valeurs des cellules qui n’ont pas encore été calculées dans ce cycle le recalcul.
    
- La fonction peut appeler une des fonctions XLM informations (classe 2), par exemple, **xlfGetCell**.
    
- Si le signe dièse (#) n’est pas présent : évaluation une cellule calculée entraîne une erreur **au niveau** et la fonction en cours est appelée à nouveau une fois que la cellule a été calculée ; appeler une fonction d’informations XLM autre que **xlfCaller** entraîne une erreur **xlretInvXlfn** . 
    
### <a name="registering-worksheet-functions-as-thread-safe"></a>Inscription des fonctions de feuille de calcul en tant que thread-safe

À compter d’Excel 2007, Excel peut effectuer le recalcul du classeur multithread. Cela signifie que plusieurs instances d’une fonction de thread-safe peut affecter aux threads simultanés pour réévaluation. À compter d’Excel 2007, la plupart des fonctions de feuille de calcul intégré est thread-safe. À compter d’Excel 2007, Excel permet également à enregistrer les fonctions de feuille de calcul en tant que thread-safe XLL. Pour ce faire, incluez un **$** caractères après le dernier code paramètre _pxTypeText_. 
  
> [!NOTE]
> Seules les fonctions de feuille de calcul peuvent être déclarées comme thread-safe. Excel ne tient pas compte une fonction équivalente de la feuille macro pour être thread-safe, afin que vous ne pouvez pas ajouter les deux **#** et **$** caractères pour l’argument _pxTypeText_ . 
  
Si vous avez enregistré une fonction en tant que thread-safe, vous devez vous assurer qu’il se comporte de façon thread-safe, bien qu’Excel rejette tous les appels non sécurisées par le biais de l’API C. Par exemple, si une fonction thread-safe tente d’appeler **xlfGetCell**, l’appel échoue avec l’erreur **xlretNotThreadSafe** . 
  
### <a name="registering-worksheet-functions-as-cluster-safe"></a>Inscription des fonctions de feuille de calcul en tant que cluster sécurisé

À compter d’Excel 2010, Excel permettre transférer des appels de fonction à un fournisseur de cluster de calcul désignés. Pour plus d’informations, voir [Fonctions sécurisées pour le Cluster](cluster-safe-functions.md). Des fonctions de feuille de calcul XLL enregistrées en tant que cluster-safe prennent part du déchargement si un cluster est disponible. Fonctions sécurisées pour le cluster sont inscrits en incluant le **&amp;** caractères après le dernier code de paramètre dans l’argument _pxTypeText_ . 
  
Si vous avez enregistré une fonction comme sécurisées pour le cluster, vous devez vous assurer qu’il se comporte de façon sécurisées pour le cluster. Pour plus d’informations, voir [Fonctions sécurisées pour le Cluster](cluster-safe-functions.md).
  
> [!NOTE]
> Seules les fonctions de feuille de calcul peuvent être déclarées comme sécurisées pour le cluster. Excel ne tient pas compte une fonction équivalente de la feuille macro être sécurisées pour le cluster, afin que vous ne pouvez pas ajouter les deux **#** et **&amp;** caractères pour l’argument _pxTypeText_ . Fonctions de feuille de calcul peuvent être déclarées comme sécurisées pour le cluster et thread-safe. Dans ce cas, Excel permettra de ces fonctions à prendre part à un nouveau calcul multithread lors du déchargement de cluster est désactivé. 
  
### <a name="category-names"></a>Noms de catégorie

Utilisez les instructions suivantes pour déterminer quelle catégorie de placer votre XLL fonctionne dans.
  
- Si la fonction effectue une action qui peut être réalisé par l’utilisateur dans le cadre de votre interface utilisateur du complément, vous devez placer la fonction de la catégorie de **commandes** . 
    
- Si la fonction renvoie des informations sur l’état de la macro complémentaire ou toute autre information utile, vous devez placer la fonction de la catégorie **d’informations** . 
    
- Un complément doit ajouter jamais fonctions ou des commandes à la catégorie **Définie par l’utilisateur** . Cette catégorie est à l’usage exclusif des utilisateurs finaux. 
    
La catégorie est spécifiée à l’aide du paramètre _pxCategory_ de **xlfRegister**. Il peut s’agir d’un nombre ou du texte qui correspond à l’une des catégories standards codé en dur ou le texte d’une nouvelle catégorie spécifiée par la DLL. Si le texte n’existe pas déjà, Excel crée une nouvelle catégorie portant ce nom.
  
Le tableau suivant répertorie les catégories standards qui sont visibles lorsque vous affichez la boîte de dialogue **Coller une fonction** à partir d’une feuille de calcul. 
  
|**Number**|**Text**|
|:-----|:-----|
|1  <br/> |Finances  <br/> |
|2  <br/> |Date &amp; heure  <br/> |
|3  <br/> |Math &amp; trigonométrique  <br/> |
|4  <br/> |Texte  <br/> |
|5  <br/> |Logique  <br/> |
|6  <br/> |Recherche &amp; référence  <br/> |
|7  <br/> |Base de données  <br/> |
|8  <br/> |Statistiques  <br/> |
|9  <br/> |Information  <br/> |
|14  <br/> |Personnalisées  <br/> |
||Ingénierie (commençant dans Excel 2007)  <br/> |
||Cube (commençant dans Excel 2007)  <br/> |
   
En outre, les catégories suivantes sont également visibles lorsque vous affichez la boîte de dialogue **Coller une fonction** à partir d’une feuille macro. 
  
|**Number**|**Text**|
|:-----|:-----|
|10  <br/> |Commandes  <br/> |
|11  <br/> |DDE/Externe  <br/> |
|12  <br/> |Personnalisation  <br/> |
|13  <br/> |Contrôle de macros  <br/> |
   
### <a name="example"></a>Exemple

Voir le code de la fonction **xlAutoOpen** dans `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Voir aussi

- [REGISTRE.](xlfregisterid.md)
- [ANNULER L’INSCRIPTION](xlfunregister-form-1.md)
- [Fonctions XLM d’API C utiles et essentielles](essential-and-useful-c-api-xlm-functions.md)

