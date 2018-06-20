---
title: Développement de DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLL [excel 2007], création, la création de DLL [Excel 2007]
localization_priority: Normal
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 030cdd4358d9a71841eca6acfcef6e71839e02a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782038"
---
# <a name="developing-dlls"></a>Développement de DLL

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Une bibliothèque est un corps de code compilé qui fournit des fonctionnalités et des données à une application exécutable. Bibliothèques peuvent être liées statiquement ou liées de manière dynamique, et traditionnellement ont les .lib d’extensions de nom de fichier .dll respectivement. Bibliothèques statiques (par exemple, la bibliothèque Runtime C) sont liés à l’application au niveau de compilation et donc font partie de l’exécutable qui en résulte. L’application charge une DLL lorsqu’il est nécessaire, généralement au démarrage de l’application. Une DLL peut charger et lier dynamiquement à une autre DLL.
  
## <a name="benefits-of-using-dlls"></a>Avantages de l’utilisation des DLL

Les principaux avantages des DLL sont les suivantes :
  
- Toutes les applications peuvent partager une seule copie sur le disque.
    
- Les fichiers exécutables des applications sont conservés plus petits.
    
- Ils permettent aux projets de développement grande être réparties. Les développeurs d’application et la DLL doivent accepter une interface entre leurs composants respectifs. Cette interface est exportée par la DLL.
    
- Les développeurs DLL peuvent mettre à jour les DLL — par exemple, pour les rendre plus efficace ou pour résoudre un bogue, sans avoir à mettre à jour toutes les applications qui l’utilisent, à condition que l’interface de la DLL exportée ne change pas.
    
Vous pouvez utiliser la DLL pour ajouter des fonctions de feuille de calcul et les commandes dans Microsoft Excel.
  
## <a name="resources-for-creating-dlls"></a>Ressources pour la création de DLL

Pour créer une DLL, vous devez les éléments suivants :
  
- Un éditeur de code source.
    
- Un compilateur pour activer le code source dans le code de l’objet qui est compatible avec votre matériel.
    
- Un éditeur de liens pour ajouter du code à partir de bibliothèques statiques, où les utilisées et pour créer le fichier exécutable de la DLL.
    
Fournissent des environnements modernes de développement intégré (IDE), tel que Microsoft Visual Studio, tous ces éléments. Elles fournissent également beaucoup plus : actives éditeurs, outils de débogage de votre code, outils permettant de gérer plusieurs projets, de nouveaux Assistants de projet et de nombreux autres outils importants.
  
Vous pouvez créer des DLL dans plusieurs langues, par exemple, C/C++, Pascal et Visual Basic. Étant donné que l’API de code source fourni avec Excel est C et C++, seuls ces deux langages sont considérés comme dans cette documentation.
  
## <a name="exporting-functions-and-commands"></a>Exportation des fonctions et les commandes

Lors de la compilation d’un projet de DLL, le compilateur et l’éditeur de liens doivent connaître les fonctions qui sont à exporter afin qu’ils peuvent être disponibles à l’application. Cette section décrit les moyens de que le faire.
  
Lorsque les compilateurs compilent le code source, en général, ils modifient les noms des fonctions à partir de leur affichage dans le code source. Ils généralement cela en ajoutant le début et/ou à la fin du nom, dans un processus appelé ornement de nom. Vous devez vous assurer que la fonction est exportée par un nom reconnaissable à l’application de chargement de la DLL. Cela peut signifier pour présenter à l’éditeur de liens pour associer le nom décoré avec un nom plus simple d’exportation. Le nom de l’exportation peut être le nom tel qu’il apparaissait à l’origine dans le code source, ou autre chose.
  
La façon dont le nom est décoré dépend de la langue et la façon dont le compilateur est invité à mettre à la disposition, la fonction autrement dit, la convention d’appel. Convention d’appel entre les processus standard de Windows utilisés par les DLL est appelée la convention WinAPI. Il est défini dans les fichiers d’en-tête Windows en tant que **WINAPI**, qui est définie à son tour à l’aide de la de déclarateur Win32 **__stdcall**.
  
Une fonction d’exportation de la DLL pour une utilisation avec Excel (si elle est une fonction de feuille de calcul, fonction équivalente feuille macro ou commande définie par l’utilisateur) doit toujours utiliser le **WINAPI** / convention d’appel **__stdcall** . Il est nécessaire d’inclure le spécificateur **WINAPI** explicitement dans la définition de la fonction que la valeur par défaut dans Win32 compilateurs consiste à utiliser la **__cdecl** convention d’appel, également définie en tant que **WINAPIV**, si aucun n’est spécifié.
  
Vous pouvez indiquer à l’éditeur de liens qui une fonction doit être exporté et le nom qu’il est à l’extérieur de plusieurs façons :
  
- Placez la fonction dans un fichier de définition après le mot clé **EXPORTE** et définir votre projet DLL pour faire référence à ce fichier lors de la liaison. 
    
- Utilisez le déclarateur **__declspec (dllexport)** dans la définition de la fonction. 
    
- Utilisez une directive de préprocesseur **#pragma** pour envoyer un message à l’éditeur de liens. 
    
Bien que votre projet peut utiliser ces trois méthodes et votre compilateur et l’éditeur de liens prennent en charge les, vous devriez pas exporter une fonction dans plus d’une des manières suivantes. Par exemple, supposons qu’une DLL contient les modules de code source deux, C et un langage C++, qui contient deux fonctions à exporter, **Mon\_C\_exporter** et **Mon\_RPC\_exporter** respectivement. Par souci de simplicité, supposons que chaque fonction prend un seul argument numérique double précision et renvoie le même type de données. Les possibilités d’exportation de chaque fonction à l’aide de chacune de ces méthodes sont décrites dans les sections suivantes. 
  
### <a name="using-a-def-file"></a>À l’aide d’un fichier de définition

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

<br/>

Le fichier DEF devra puis contient ces lignes.
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

La syntaxe générale d’une ligne qui suit une instruction **exportations** est comme suit. 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

Notez que la fonction C a été décorée, mais le fichier DEF force explicitement l’éditeur de liens pour exposer la fonction en utilisant le nom de code source d’origine (dans cet exemple). L’éditeur de liens exporte implicitement la fonction C++ en utilisant le nom de code d’origine, afin qu’il ne soit pas nécessaire d’inclure le nom décoré dans le fichier de définition.
  
Pour les appels de fonction API Windows 32 bits, la convention pour l’habillage graphique des fonctions compilé-C est la suivante : **nom de la fonction** devient le **nom de la fonction @** _ _n_ où _n_ est le nombre d’octets exprimée sous la forme d’un nombre décimal pris en charge par tous les arguments, les octets pour chaque arrondi au multiple plus proche de quatre. 
  
> [!NOTE]
> Tous les pointeurs sont les quatre octets dans Win32. Le type de retour a aucun impact sur ornement de nom. 
  
Il est possible d’obliger le compilateur C++ pour exposer des noms non décorés des fonctions C++ en mettant la fonction et les prototypes de fonction, au sein d’un « C » {...} externe bloquer, comme illustré dans cet exemple. (Les accolades **{}** sont tous deux omis ici car la déclaration fait référence uniquement pour le bloc de code de fonction qui suit immédiatement). 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

Lorsque vous placez prototypes de fonction C dans les fichiers d’en-tête qui peuvent être inclus dans les fichiers source C ou C++, vous devez inclure la directive de préprocesseur suivante.
  
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

### <a name="using-the-declspecdllexport-declarator"></a>À l’aide de la déclarateur __declspec (dllexport)

Le mot clé **__declspec (dllexport)** peut être utilisé dans la déclaration de la fonction comme suit. 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

Le mot clé **__declspec (dllexport)** doit être ajouté à l’extrême gauche de la déclaration. Les avantages de cette approche sont que la fonction ne doit pas figurer dans un fichier de définition, et que l’état de l’exportation est à la définition. 
  
Si vous souhaitez éviter une fonction C++ seront disponible avec l’ornement de nom C++, vous devez déclarer la fonction comme suit.
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

L’éditeur de liens rend la fonction disponibles en tant que my_undecorated_Cpp_export, autrement dit, le nom tel qu’il apparaît dans le code source avec aucun ornement.
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a>À l’aide d’une directive de l’éditeur de liens préprocesseur #pragma

Dernières versions de Microsoft Visual Studio prend en charge deux macros prédéfinies qui, lorsqu’elle est utilisée conjointement avec une directive **#pragma** , permettent de demander à l’éditeur de liens pour exporter la fonction directement dans le code de la fonction. Les macros sont __fonction__ et __FUNCDNAME__ (Notez la double souligné à chaque fin) qui sont développées pour les noms de fonction non décorée et décorée respectivement. 
  
Par exemple, lorsque vous utilisez Microsoft Visual Studio, ces lignes peuvent être intégrés comme suit dans un fichier d’en-tête courants.
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

Si cet en-tête est inclus dans les fichiers source, les fonctions de deux exemples peuvent ensuite être exportées comme suit.
  
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

Notez que la directive doit être placée dans le corps de la fonction et est développée uniquement lorsque aucune des options du compilateur **/EP** ou **/P** est défini. Cette technique élimine le besoin d’un fichier de définition ou déclaration **__declspec (dllexport)** et conserve la spécification de son état d’exportation avec le code de la fonction. 
  
## <a name="see-also"></a>Voir aussi

- [Accès aux DLL dans Excel](how-to-access-dlls-in-excel.md)
- [Appel dans Excel � partir du fichier DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md)
- [Concepts de programmation Excel](excel-programming-concepts.md)
- [D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)

