---
title: Développement de DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLL [Excel 2007], création, création de DLL [Excel 2007]
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
ms.localizationpriority: high
ms.openlocfilehash: c84b115e259f1ccee9ead677ce1285c9db606dc2
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62459094"
---
# <a name="developing-dlls"></a>Développement de DLL

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Une bibliothèque est une collection de code compilé qui fournit des fonctionnalités et des données à une application exécutable. Les bibliothèques peuvent être liées statiquement ou dynamiquement et ont conventionnellement les extensions de nom de fichier .lib et .dll, respectivement. Les bibliothèques statiques (par exemple, la bibliothèque en C) sont liées à l’application lors de la compilation et font donc partie intégrante de l’exécutable qui en résulte. L’application charge une DLL lorsque nécessaire, généralement au démarrage de l’application. Une DLL peut charger et établir un lien dynamiquement vers une autre DLL.
  
## <a name="benefits-of-using-dlls"></a>Avantages de l'utilisation des DLL

Les principaux avantages des DLL sont les suivants :
  
- Toutes les applications peuvent partager une copie unique sur disque.
    
- Les fichiers exécutables des applications sont plus petits.
    
- Ils permettent de diviser les projets de développement volumineux. Les développeurs d’application et de DLL doivent uniquement se mettre chacun d’accord sur une interface. Cette interface est exportée par la DLL.
    
- Les développeurs de DLL peuvent mettre à jour les DLL (pour augmenter leur efficacité ou corriger un bogue, par exemple) sans avoir à mettre à jour toutes les applications qui l’utilisent, tant que l’interface exportée de la DLL ne change pas.
    
Vous pouvez utiliser les DLL pour ajouter des commandes et les fonctions de feuille de calcul dans Microsoft Excel.
  
## <a name="resources-for-creating-dlls"></a>Ressources pour la création de DLL

Pour créer une DLL, vous devez disposer des éléments suivants :
  
- un éditeur de code source ;
    
- un compilateur pour transformer le code source en code objet compatible avec votre matériel ;
    
- un éditeur de liens pour ajouter du code à partir de bibliothèques statiques, le cas échéant, et pour créer le fichier DLL exécutable.
    
Les environnements de développement intégré moderne (IDE), tels que Microsoft Visual Studio, fournissent tous ces éléments. Ils fournissent également d’autres éléments : éditeurs intelligents, outils pour déboguer votre code, outils pour gérer plusieurs projets, nouveaux assistants de projet et de nombreux autres outils importants.
  
Vous pouvez créer des DLL en plusieurs langages : C/C++, Pascal et Visual Basic, par exemple. Étant donné que le code source API fourni avec Excel est C et C++, ces deux langages sont pris en compte dans cette documentation.
  
## <a name="exporting-functions-and-commands"></a>Exportation de fonctions et de commandes

Lors de la compilation d’un projet DLL, le compilateur et l’éditeur de liens doivent savoir quelles fonctions doivent être exportées afin de pouvoir les rendre accessibles à l’application. Cette section décrit les façons de procéder.
  
Lorsque les compilateurs compilent le code source, en général, ils modifient les noms des fonctions à partir de leur apparence dans le code source. Pour ce faire, ils effectuent un ajout généralement à la fin et/ou au début du nom, lors d’un processus appelé décoration de nom. Vous devez vérifier que la fonction est exportée avec un nom reconnaissable pour l’application qui charge la DLL. Ainsi, il est possible d’indiquer à l’éditeur de liens d’associer le nom décoré à un nom d’exportation plus simple. Le nom d’exportation peut être le nom tel qu’il apparaissait à l’origine dans le code source, ou quelque chose d’autre.
  
La façon dont le nom est décoré dépend du langage et de la façon dont le compilateur doit rendre la fonction disponible, autrement dit, la convention d’appel. La convention d’appel standard entre les processus pour Windows utilisée par les DLL est appelée la convention WinAPI. Elle est définie dans les fichiers d’en-tête Windows sous la forme **WINAPI**, définie à son tour en utilisant le déclarateur Win32 **__stdcall**.
  
Une fonction d’exportation DLL à utiliser avec Excel (fonction de feuille de calcul, fonction équivalente à une feuille macro ou commande définie par l’utilisateur) doit toujours utiliser la convention d’appel **WINAPI** / **__stdcall**. Il faut inclure le spécificateur **WINAPI** explicitement dans la définition de la fonction car, par défaut, dans les compilateurs Win32, la convention d’appel **__cdecl** (également définie comme **WINAPIV**) est utilisée, si aucune n’est spécifiée.
  
Vous pouvez indiquer à l’éditeur de liens qu’une fonction doit être exportée et son nom doit être connu de manière externe de plusieurs manières :
  
- Placez la fonction dans un fichier DEF après le mot clé **EXPORTS** et définissez votre paramètre de projet DLL pour référencer ce fichier lors de la liaison. 
    
- Utilisez le déclarateur **__declspec (dllexport)** dans la définition de la fonction. 
    
- Utilisez une directive de préprocesseur **#pragma** pour envoyer un message à l’éditeur de liens. 
    
Même si votre projet peut utiliser les trois méthodes, qui sont prises en charge par votre compilateur et l’éditeur de liens, mais vous ne devez pas essayer d’exporter une fonction de plusieurs façons. Par exemple, supposons qu’une DLL contient deux modules de code source (un C et un C++) qui contiennent deux fonctions à exporter, **my\_C\_export** et **my\_Cpp\_export**, respectivement. Pour simplifier, supposons que chaque fonction prend un argument numérique double précision unique et renvoie le même type de données. Les autres façons d’exporter chaque fonction à l’aide de chacune de ces méthodes sont décrites dans les sections suivantes. 
  
### <a name="using-a-def-file"></a>Utilisation d’un fichier DEF

```C
double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

```cpp
double WINAPI my_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```


Le fichier DEF doit alors contenir ces lignes :
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`


La syntaxe générale d’une ligne qui suit une instruction **EXPORTS** est : 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

Notez que la fonction C a été décorée, mais le fichier DEF force explicitement l’éditeur de liens à exposer la fonction en utilisant le nom de code source d’origine (dans cet exemple). L’éditeur de liens exporte implicitement la fonction C++ en utilisant le nom de code d’origine, pour éviter d’inclure le nom décoré dans le fichier DEF.
  
Pour les appels de fonction API Windows 32 bits, la convention pour la décoration des fonctions compilées en C est la suivante : **function_name** devient _ **function_name@** _n_ où _n_ correspond au nombre d’octets exprimé sous la forme d’un nombre décimal pris par tous les arguments, avec les octets pour chacun arrondi au multiple de quatre le plus proche. 
  
> [!NOTE]
> La taille de tous les pointeurs dans Win32 est de quatre octets. Le type de renvoi n’a aucun impact sur la décoration de nom. 
  
Il est possible de forcer le compilateur C++ à exposer des noms non décorés pour les fonctions C++ en encadrant la fonction et les prototypes de fonction, dans un bloc externe "C" {…}, comme illustré dans cet exemple. (Les accolades **{}** sont omises ici, car la déclaration fait référence uniquement au bloc de code de fonction qui la suit immédiatement). 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

Lorsque vous placez des prototypes de fonction C dans des fichiers d’en-tête qui pourraient être inclus dans des fichiers source C ou C++, vous devez inclure la directive de préprocesseur suivante.
  
```cpp
#ifdef __cplusplus
extern "C" {
#endif
double WINAPI my_C_export(double x);
double WINAPI my_Cdecorated_Cpp_export(double x);
#ifdef __cplusplus
}
#endif
```

### <a name="using-the-__declspecdllexport-declarator"></a>Utilisation du déclarateur __declspec (dllexport)

Le mot clé **__declspec (dllexport)** peut être utilisé dans la déclaration de la fonction comme suit. 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

Le mot clé **__declspec (dllexport)** doit être ajouté tout à fait à gauche de la déclaration. Les avantages de cette approche sont les suivants : la fonction ne doit pas être répertoriée dans un fichier DEF et le statut d’exportation est avec la définition. 
  
Si vous souhaitez éviter une fonction C++ rendue disponible avec la décoration de nom C++, vous devez déclarer la fonction comme suit.
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

L’éditeur de liens rend la fonction disponible sous la forme my_undecorated_Cpp_export, autrement dit, le nom tel qu’il apparaît dans le code source sans aucune décoration.
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a>Utilisation d’une directive de l’éditeur de liens du préprocesseur #pragma

Les versions récentes de Microsoft Visual Studio prennent en charge deux macros prédéfinies qui, lorsqu’elles sont utilisées conjointement avec une directive **#pragma**, vous permettent de demander à l’éditeur de liens d’exporter la fonction directement à partir du code de fonction. Les macros sont __FUNCTION__ et __FUNCDNAME__ (notez le double trait de soulignement à chaque extrémité) qui sont développées pour les noms de fonction non décorés et décorés, respectivement. 
  
Par exemple, lorsque vous utilisez Microsoft Visual Studio, ces lignes peuvent être incorporées dans un fichier d’en-tête courant comme suit.
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

Si cet en-tête est inclus dans les fichiers source, les deux exemples de fonctions peuvent ensuite être exportés comme suit.
  
Code C :
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

Code C++ :
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

Notez que la directive doit être placée dans le corps de la fonction et est développée uniquement lorsque aucune des options du compilateur **/EP** ni **/P** n’est définie. Grâce à cette technique, aucun fichier DEF ni déclaration **__declspec(dllexport)** n’est nécessaire, et la spécification de son état d’exportation reste avec le code de fonction. 
  
## <a name="see-also"></a>Voir aussi

- [Accès aux DLL dans Excel](how-to-access-dlls-in-excel.md)
- [Appel dans Excel à partir du fichier DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md)
- [Concepts de programmation Excel](excel-programming-concepts.md)
- [Développement de XLL de Excel](developing-excel-xlls.md)

