---
title: Compatibilité descendante
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilité des versions [excel 2007], compatibilité XLL [Excel 2007], [Excel 2007] de compatibilité descendante
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387971"
---
# <a name="backward-compatibility"></a>Compatibilité descendante

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Cette rubrique traite des problèmes de compatibilité XLL dans différentes versions de Microsoft Excel.
  
## <a name="useful-constant-definitions"></a>Définitions utiles

Envisager d’inclure des définitions similaires à celles-ci dans le code de votre projet XLL et remplacer toutes les instances de valeurs littérales utilisées dans ce contexte. Cela clarifier le code qui est la version spécifique et réduire les risques de bogues version sous la forme de nombres inoffensive.
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a>Obtention de la version en cours d’exécution

Vous devez détecter la version est en cours d’exécution à l’aide de `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, où `arg` numérique **XLOPER** la valeur 2 et la version est une chaîne **XLOPER** qui peut ensuite être converti en entier. Pour Microsoft Excel 2013, il s’agit 15.0. Vous devez procéder dans, ou à partir de la fonction [xlAutoOpen](xlautoopen.md) . Vous pouvez ensuite définir une variable globale qui informe tous les modules dans votre projet de la version d’Excel est en cours d’exécution. Votre code peut ensuite décider s’il faut appeler l’API C en utilisant **Excel12** et **XLOPER12**s, ou **Excel4** à l’aide de s **XLOPER**.
  
Vous pouvez appeler **XLCallVer** pour découvrir la version de l’API C, mais cela n’indique pas les versions à Excel 2007 vous sont en cours d’exécution. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Création de compléments exportant des interfaces doubles

Envisagez une fonction XLL qui accepte une chaîne et renvoie une valeur qui peut être un des types de données de feuille de calcul. Vous pouvez exporter une fonction inscrit comme tapez « PD » et prototyper comme suit où la chaîne est transmise comme une chaîne d’octets.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Bien que ce scénario fonctionne parfaitement, il existe plusieurs raisons pour lesquelles ce n’est pas l’interface idéale à votre code à compter d’Excel 2007 :
  
- Il est soumis aux limitations de chaînes d’octets API C et ne peut pas accéder aux longues chaînes Unicode pris en charge à compter d’Excel 2007.
    
- Bien que, à compter d’Excel 2007, Excel peut passer et accepter **XLOPER**s, en interne il les convertit en **XLOPER12**s, donc il existe une surcharge de conversion implicite à compter d’Excel 2007 qui n’est pas il lorsque le code s’exécute dans les versions antérieures d’Excel.
    
- Il peut s’avérer que cette fonction peut être rendue thread-safe, mais si la chaîne type est remplacée par `PD$`, l’enregistrement échoue lors du démarrage avant d’Excel 2007.
    
Pour ces raisons, dans l’idéal, compter d’Excel 2007, vous devez exporter une fonction pour vos utilisateurs qui a été enregistré en tant que `QD%$`, en supposant que votre code est thread-safe et prototyper comme suit.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Une autre raison pourquoi vous souhaiterez peut-être enregistrer une autre fonction à compter d’Excel 2007 est afin de permettre aux fonctions XLL d’accepter jusqu'à 255 arguments, au lieu de la limite des versions antérieures de 30.
  
Heureusement, vous pouvez avoir les avantages des deux en exportant les deux versions de votre projet. Vous pouvez ensuite détecter la version d’Excel en cours d’exécution et conditionnellement enregistrer la fonction la plus appropriée. Pour plus d’informations et un exemple d’implémentation, voir [Developing compléments (XLL) dans Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).
  
Cette approche la possibilité qu’une feuille de calcul en cours d’exécution dans Excel 2003 peut afficher des résultats différents de la même feuille en cours d’exécution à compter d’Excel 2007. Par exemple, Microsoft Excel 2003 souhaite mapper une chaîne Unicode dans une cellule de feuille de calcul Excel 2003 à une chaîne d’octets ASCII, tronqué avant de passer à une fonction XLL. À compter d’Excel 2007, Excel passe une chaîne Unicode non convertie à une fonction XLL inscrite dans la bonne manière. Cela peut entraîner un résultat différent. Vous devez être conscient de cette possibilité et les conséquences de vos utilisateurs, pas seulement dans la mise à niveau. Par exemple, certaines fonctions numériques intégrées ont été améliorées entre Excel 2000 et Excel 2003.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Nouvelles fonctions de feuille de calcul et des fonctions de l’utilitaire d’analyse

Fonctions utilitaire d’analyse font partie d’Excel à compter d’Excel 2007. Auparavant, un XLL pouvait appeler uniquement une fonction DAV à l’aide de [xlUDF](xludf.md). À compter d’Excel 2007, les fonctions DAV doivent être appelées à l’aide les énumérations de fonction définies dans xlcall.h. L’exemple de fonctions définies par l’utilisateur de l’appel à partir de DLL montre les deux méthodes différentes.
  
## <a name="see-also"></a>Voir aussi

- [Les fonctions de rappel de l'API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programmation avec l�API C dans Excel](programming-with-the-c-api-in-excel.md)
- [Nouveautés dans l’API C pour Excel](what-s-new-in-the-c-api-for-excel.md)

