---
title: Compatibilité descendante
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilité de version [excel 2007],compatibilité XLL [Excel 2007],compatibilité ascendante [Excel 2007]
ms.localizationpriority: medium
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 25f4a4b3b47a84846ab0f5ef424d535765a78515
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588384"
---
# <a name="backward-compatibility"></a>Compatibilité descendante

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Cette rubrique traite des problèmes de compatibilité XLL dans différentes versions de Microsoft Excel.
  
## <a name="useful-constant-definitions"></a>Définitions de constantes utiles

Envisagez d’inclure des définitions similaires à celles-ci dans le code de votre projet XLL et de remplacer toutes les instances de nombres littéraux utilisés dans ce contexte. Cela permet de clarifier le code propre à la version et de réduire la probabilité de bogues liés à la version sous la forme de numéros sans effet.
  
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

Vous devez détecter quelle version est en cours d’exécution, où est une XLOPER numérique définie sur 2 et la version est une `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)` `arg` chaîne **XLOPER**  qui peut ensuite être contrainte en un nombre. Par Microsoft Excel 2013, il s’agit de 15.0. Vous devez le faire dans la fonction [xlAutoOpen](xlautoopen.md) ou à partir de celle-ci. Vous pouvez ensuite définir une variable globale qui informe tous les modules de votre projet sur la version de Excel en cours d’exécution. Votre code peut ensuite décider d’appeler l’API C à l’aide **d’Excel12** et **xlOPER12** ou d’Excel4 à l’aide **de XLOPER.** 
  
Vous pouvez appeler **XLCallVer** pour découvrir la version de l’API C, mais cela n’indique pas quelle version pré-Excel 2007 que vous exécutez. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Création de add-ins qui exportent des interfaces doubles

Considérons une fonction XLL qui prend une chaîne et renvoie une valeur qui peut être n’importe quel type de données de feuille de calcul. Vous pouvez exporter une fonction enregistrée en tant que type « PD » et prototyped comme suit, où la chaîne est passée en tant que chaîne d’byte comptée de longueur.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Bien que cela fonctionne parfaitement, il existe plusieurs raisons pour lesquelles il ne s’agit pas de l’interface idéale pour votre code à partir de Excel 2007 :
  
- Il est soumis aux limitations des chaînes d’byte de l’API C et ne peut pas accéder aux chaînes Unicode longues prise en charge à partir de Excel 2007.
    
- Bien que, à partir de Excel 2007, Excel puisse passer et accepter des **XLOPER,** en interne il les convertit en **XLOPER12,** il existe donc une surcharge de conversion implicite à partir de Excel 2007 qui n’existe pas lorsque le code s’exécute dans les versions antérieures de Excel.
    
- Cette fonction peut être rendue thread-safe, mais si la chaîne de type est modifiée, l’inscription échoue au démarrage avant `PD$` Excel 2007.
    
Pour ces raisons, dans l’idéal, à partir de Excel 2007, vous devez exporter une fonction pour vos utilisateurs qui a été inscrite en tant que , en supposant que votre code est thread-safe et prototyped comme `QD%$` suit.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Une autre raison pour laquelle vous souhaitez peut-être inscrire une autre fonction à partir de Excel 2007 est qu’elle autorise les fonctions XLL à prendre jusqu’à 255 arguments, au lieu de la limite de 30 versions antérieures.
  
Heureusement, vous pouvez bénéficier des deux avantages en exportant les deux versions à partir de votre projet. Vous pouvez ensuite détecter la version Excel en cours d’exécution et inscrire de manière conditionnable la fonction la plus appropriée. Pour plus d’informations et un exemple d’implémentation, voir [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).
  
Cette approche conduit à la possibilité qu’une feuille de calcul s’exécutant dans Excel 2003 puisse afficher des résultats différents de ceux de la même feuille en cours d’exécution depuis Excel 2007. Par exemple, Excel 2003 maque une chaîne Unicode dans une cellule de feuille de calcul Excel 2003 à une chaîne d’byte-ASCII et la tronque avant de la transmettre à une fonction XLL. À compter Excel 2007, Excel passe une chaîne Unicode non inversée à une fonction XLL inscrite de la bonne façon. Cela peut entraîner un résultat différent. Vous devez être conscient de cette possibilité et des conséquences pour vos utilisateurs, pas seulement dans la mise à niveau. Par exemple, certaines fonctions numériques intégrées ont été améliorées entre Excel 2000 et Excel 2003.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Nouvelles fonctions de feuille de calcul et fonctions de la boîte à outils Analyse

Les fonctions de la boîte à outils Analysis Toolpak (ATP) font partie Excel à partir Excel 2007. Auparavant, une XLL pouvait uniquement appeler une fonction ATP à l’aide [de xlUDF](xludf.md). À compter Excel 2007, les fonctions ATP doivent être appelées à l’aide des éumérations de fonction définies dans xlcall.h. L’exemple dans Calling User-defined Functions from DLLs illustre les deux méthodes différentes.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions de rappel de l’API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programmation avec l�API C dans Excel](programming-with-the-c-api-in-excel.md)
- [Quelles sont les nouveaut�s de l'API C pour Excel 2013](what-s-new-in-the-c-api-for-excel.md)

