---
title: Compatibilité descendante
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilité des versions [Excel 2007], compatibilité XLL [Excel 2007], compatibilité descendante [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301679"
---
# <a name="backward-compatibility"></a>Compatibilité descendante

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Cette rubrique traite des problèmes de compatibilité XLL dans les différentes versions de Microsoft Excel.
  
## <a name="useful-constant-definitions"></a>Définitions des constantes utiles

EnVisagez d'inclure des définitions similaires à celles-ci dans votre code de projet XLL et de remplacer toutes les instances de nombres littéraux utilisés dans ce contexte. Cela permet de clarifier le code dont la version est propre et de réduire les risques de bogues liés à la version sous la forme de numéros inoffensifs.
  
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

## <a name="getting-the-running-version"></a>Obtention de la version en cours d'exécution

Vous devez détecter quelle version est en cours `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`d'exécution `arg` à l'aide de, où est un **XLOPER** numérique défini sur 2 et version est une chaîne **XLOPER** qui peut ensuite être forcée sur un entier. Pour Microsoft Excel 2013, il s'agit de 15,0. Vous devez effectuer cette opération dans, ou à partir de, la fonction [xlAutoOpen](xlautoopen.md) . Vous pouvez ensuite définir une variable globale qui informe tous les modules de votre projet de la version d'Excel qui est en cours d'exécution. Votre code peut ensuite décider s'il faut appeler l'API C à l'aide de **Excel12** et de **XLOPER12**, ou en utilisant **Excel4** à l'aide de **XLOPER**s.
  
Vous pouvez appeler **XLCallVer** pour découvrir la version de l'API C, mais cela n'indique pas laquelle des versions antérieures d'Excel 2007 sont en cours d'exécution. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Création de compléments qui exportent des interfaces doubles

Considérez une fonction XLL qui prend une chaîne et renvoie une valeur qui peut être n'importe quel type de données de feuille de calcul. Vous pouvez exporter une fonction inscrite en tant que type «lib» et prototypée comme suit lorsque la chaîne est transmise sous la forme d'une chaîne d'octets de longueur comptée.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Bien que cela fonctionne parfaitement bien, il existe plusieurs raisons pour lesquelles il ne s'agit pas de l'interface idéale pour votre code en commençant dans Excel 2007:
  
- Elle est soumise aux limitations des chaînes d'octets de l'API C et ne peut pas accéder aux chaînes Unicode longues prises en charge à partir d'Excel 2007.
    
- Bien que, en commençant dans Excel 2007, Excel puisse transmettre et accepter des éléments **XLOPER**, en interne, il les convertit en éléments **XLOPER12**, de sorte qu'il existe une charge de conversion implicite en commençant par Excel 2007, lorsque le code s'exécute dans les versions antérieures d'Excel.
    
- Cette fonction peut être rendue thread-safe, mais si la chaîne de `PD$`type est changée en, l'inscription échoue avant Excel 2007.
    
Pour ces raisons, dans l'idéal, en commençant dans Excel 2007, vous devez exporter une fonction pour les utilisateurs `QD%$`qui ont été enregistrés sous, en supposant que votre code est thread-safe et prototypée comme suit.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Une autre raison pour laquelle vous pouvez souhaiter enregistrer une fonction différente en commençant dans Excel 2007 est qu'elle permet aux fonctions XLL de prendre jusqu'à 255 arguments au lieu de la limite de 30 versions antérieures.
  
Heureusement, vous pouvez bénéficier des avantages des deux en exportant les deux versions de votre projet. Vous pouvez ensuite détecter la version Excel en cours d'exécution et enregistrer de façon conditionnelle la fonction la plus appropriée. Pour plus d'informations et pour obtenir un exemple d'implémentation, voir [developIng Add-ins (XLL) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).
  
Cette approche entraîne la possibilité qu'une feuille de calcul exécutée dans Excel 2003 puisse afficher des résultats différents de ceux de la même feuille en cours d'exécution dans Excel 2007. Par exemple, Excel 2003 mappe une chaîne Unicode dans une cellule de feuille de calcul Excel 2003 à une chaîne ASCII Byte et la tronque avant de la transmettre à une fonction XLL. À partir d'Excel 2007, Excel transmet une chaîne Unicode non convertie à une fonction XLL inscrite de la manière appropriée. Cela peut entraîner un résultat différent. Vous devez être conscient de cette possibilité et des conséquences pour vos utilisateurs, pas seulement dans la mise à niveau. Par exemple, certaines fonctions numériques intégrées ont été améliorées entre Excel 2000 et Excel 2003.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Nouvelles fonctions de feuille de calcul et fonctions de l'utilitaire d'analyse

Les fonctions de l'utilitaire d'analyse (ATP) font partie d'Excel en commençant dans Excel 2007. Auparavant, un XLL pouvait uniquement appeler une fonction ATP à l'aide de [xlUDF](xludf.md). À partir d'Excel 2007, les fonctions ATP doivent être appelées à l'aide des énumérations de fonction définies dans xlcall. h. L'exemple dans l'appel de fonctions définies par l'utilisateur à partir de dll illustre les deux méthodes.
  
## <a name="see-also"></a>Voir aussi

- [Les fonctions de rappel de l'API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programmation avec l�API�C dans Excel](programming-with-the-c-api-in-excel.md)
- [Quelles sont les nouveaut�s de l'API C pour Excel 2013](what-s-new-in-the-c-api-for-excel.md)

