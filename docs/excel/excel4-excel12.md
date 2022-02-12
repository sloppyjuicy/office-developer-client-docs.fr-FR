---
title: Excel4/Excel12
manager: lindlalu
ms.date: 01/24/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12
- Excel4
keywords:
- fonction excel4 [excel 2007]
- fonctions Excel12 [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
ms.openlocfilehash: beb191be71942e61d75ac6f7418760e8e85d3fd7
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784551"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction Microsoft Excel de feuille de calcul interne, une fonction ou une commande de feuille macro, ou une commande ou une fonction spéciale XLL uniquement, à partir d’une DLL/XLL ou d’une ressource de code.
  
Toutes les versions récentes de Excel prise en charge **d’Excel4**. À compter Excel 2007, **Excel12** est pris en charge. 
  
Ces fonctions ne peuvent être appelées que si Excel a passé le contrôle à la DLL ou au XLL. Ils peuvent également être appelés lorsque Excel a passé le contrôle indirectement via un appel à Visual Basic pour Applications (VBA). Ils ne peuvent pas être appelés à un autre moment. Par exemple, ils ne peuvent pas être appelés pendant les appels à la fonction [DllMain](/windows/win32/dlls/dllmain.md) ou à d’autres moments où le système d’exploitation a appelé la DLL, ou à partir d’un thread créé par la DLL. 
  
Les [fonctions Excel4v et Excel12v](excel4v-excel12v.md) acceptent leurs arguments en tant que tableau, tandis que les fonctions **Excel4** et **Excel12** acceptent leurs arguments en tant que liste de longueur variable dans la pile. À tous les autres égards, **Excel4** se comporte de la même manière **qu’Excel4v** et **Excel12** se comporte de la même manière **qu’Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Paramètres

 _iFunction_ (**int**)
  
Nombre qui indique la commande, la fonction ou la fonction spéciale que vous voulez appeler. Pour obtenir la liste des valeurs _iFunction_ valides, consultez la section Remarques suivante. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Pointeur vers une **XLOPER** (avec **Excel4**) ou une **XLOPER12** (avec **Excel12**) qui conservera le résultat de la fonction évaluée.
  
 _iCount_ (**int**)
  
Nombre d’arguments suivants qui seront transmis à la fonction. Dans les versions Excel jusqu’en 2003, ce nombre peut être n’importe quel nombre de 0 à 30. À compter Excel 2007, ce nombre peut être n’importe quel nombre entre 0 et 255.
  
 _argument1, ..._ (**LPXLOPER** ou **LPXLOPER12**)
  
Arguments facultatifs de la fonction. Tous les arguments doivent être des pointeurs vers **des valeurs XLOPER** ou **XLOPER12** . 
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie l’une des valeurs d’un nombre **integer (int**) suivantes.
  
|**Valeur**|**Code de retour**|**Description**|
|:-----|:-----|:-----|
|0  |**xlretSuccess** |La fonction a été appelée avec succès. Cela ne signifie pas que la fonction n’Excel pas renvoyé de valeur d’erreur Excel ; pour le savoir, vous devez examiner le type et la valeur du paramètre _pxRes_ résultant.  |
|1  |**xlretAbort** |La commande ou la fonction a été interrompue anormalement (abandon interne). Cela peut se produire si une feuille macro XLM se ferme en appelant **CLOSE** ou si Excel est en mémoire. Si Excel renvoie cette erreur, la fonction d’appel doit se quitter immédiatement. La DLL est autorisée à appeler **xlFree** uniquement avant de quitter. Tous les autres appels à l’API C ne sont pas autorisés. L’utilisateur peut enregistrer n’importe quel travail de manière interactive à l’aide de la commande **Enregistrer** **dans le** menu Fichier.  |
|2  |**xlretInvXlfn** |Un numéro de fonction non valide a été fourni. Si vous utilisez des constantes du fichier d’en-tête Xlcall.h, cela ne doit pas se produire, sauf si vous appelez un appel qui n’est pas pris en charge dans la version de Excel que vous exécutez.  |
|4  |**xlretInvCount** |Un nombre d’arguments non valide a été entré. Dans les versions jusqu Excel 2003, le nombre maximal d’arguments qu’une fonction peut prendre est de 30. À compter Excel 2007, le nombre maximal est 255. Certains nécessitent un nombre fixe ou minimal d’arguments.  |
|8   |**xlretInvXloper** |Un **XLOPER ou** **XLOPER12** non valide a été transmis à la fonction ou un argument de type erroné a été utilisé.  |
|16  |**xlretStackOvfl** |Un dépassement de la pile s’est produit. Utilisez **xlStack** pour surveiller la quantité d’espace laissé sur la pile. Évitez d’allouer de très grandes matrices et structures locales (automatiques) sur la pile dans la mesure du possible ; les rendre statiques; (Notez qu’un dépassement de la pile peut se produire sans être détecté.)  |
|32  |**xlretFailed** |Échec d’une fonction équivalente à une commande. Cela équivaut à une commande de macro affichant la boîte de dialogue d’alerte d’erreur de macro.  |
|64  |**xlretUncalced** |Une tentative de déréférencement d’une cellule qui n’a pas encore été calculée a été tentée, car elle est programmée pour être recalculée après la cellule actuelle. Dans ce cas, la DLL doit retourner le contrôle Excel immédiatement. La DLL est autorisée à appeler **xlFree** uniquement avant de quitter. Tous les autres appels à l’API C ne sont pas autorisés. Pour plus d’informations sur les fonctions qui peuvent ou ne peuvent pas accéder aux valeurs des cellules qui n’ont pas été recalculées, voir Excel [Commands, Functions, and States](excel-commands-functions-and-states.md).  |
|128  |**xlretNotThreadSafe** |Une tentative d’appel d’une fonction qui n’est pas thread-safe ou qui ne l’est peut-être pas lors d’un recalcul multithread du workbook a été tentée.  À compter Excel 2007, cette valeur est renvoyée et uniquement dans les fonctions de feuille de calcul XLL déclarées thread-safe.  |
|256  |**xlRetInvAsynchronousContext** |Le handle de fonction asynchrone n’est pas valide.  Cette valeur est utilisée uniquement par Excel 2010.  |
|512  |**xlRetNotClusterSafe** |L’appel n’est pas pris en charge sur les clusters.  Cette valeur est utilisée uniquement par Excel 2010.  |

## <a name="remarks"></a>Remarques

### <a name="valid-ifunction-values"></a>Valeurs iFunction valides

Les **valeurs iFunction** valides sont l’une des constantes **xlf...** ou **xlc...** définies dans le fichier d’en-tête Xlcall.h ou l’une des fonctions spéciales suivantes.
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** |**xlEnableXLMsgs** |**xlGetInst** |**xlSheetNm** |
|**xlCoerce** |**xlFree** |**xlGetName** |**xlStack** |
|**xlDefineBinaryName** |**xlGetBinaryName** |**xlSet** |**xlUDF** |
|**xlDisableXLMsgs** |**xlGetHwnd** |**xlSheetId** ||
   
### <a name="different-types-of-functions"></a>Différents types de fonctions

 **Excel4 et** **Excel12** font la distinction entre trois classes de fonctions. Les fonctions sont classées en fonction des trois états dans lesquels les Excel peuvent appeler la DLL.
  
- La classe 1 s’applique lorsque la DLL est appelée à partir d’une feuille de calcul suite à un recalcul.
    
- La classe 2 s’applique lorsque la DLL est appelée à partir d’une macro de fonction ou d’une feuille de calcul où elle a été inscrite avec un signe de numéro (#) dans le texte du type.
    
- La classe 3 s’applique lorsqu’une DLL est appelée à partir d’un objet, d’une macro, d’un menu, d’une barre d’outils, d’une touche de raccourci, **d’une méthode ExecuteExcel4Macro** ou de la commande **Outils/Macro/Exécuter** . Pour plus d’informations, [voir Excel Commands, Functions et States](excel-commands-functions-and-states.md).
    
Le tableau suivant indique les fonctions valides dans chaque classe.
  
|**Classe 1**|**Classe 2**|**Classe 3**|
|:-----|:-----|:-----|
|N’importe quelle fonction de feuille de calcul Toute XLL uniquement **xl...** fonction à l’exception **de xlSet**.  **xlfCaller** |N’importe quelle fonction de feuille de calcul Any **xl...** à l’exception **de xlSet**.  Fonctions de feuille macro, y compris **xlfCaller**, qui retournent une valeur mais n’effectuent aucune action qui affecte l’espace de travail ou tout classeur ouvert.  |N’importe quelle fonction, **y compris xlSet** et les fonctions équivalentes aux commandes.  |
   
### <a name="display-the-dialog-box-for-a-command-equivalent-function"></a>Afficher la boîte de dialogue d’une Command-Equivalent de boîte de dialogue

Si une fonction équivalente à une commande est associée à une boîte de dialogue, vous pouvez définir le bit **xlPrompt** dans **iFunction**. Cela signifie que Excel affiche la boîte de dialogue appropriée avant d’exécuter la commande.
  
### <a name="write-international-dlls"></a>Écriture de DLLs internationales

Si vous définissez le bit **xlIntl** dans **iFunction**, la fonction ou la commande est exécutée comme si elle était appelée à partir d’une feuille macro internationale. Cela signifie que la commande se comporte comme elle le ferait sur la version américaine de Excel, même si elle est en cours d’exécution sur une version internationale (localisée).
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced ou xlretAbort

Après avoir reçu l’une de ces valeurs de retour, votre DLL doit nettoyer et retourner le contrôle Excel immédiatement. Les rappels dans Excel via l’API C, à l’exception de **xlFree**, sont désactivés après la réception de l’une de ces valeurs de retour.
  
## <a name="example"></a>Exemple

L’exemple suivant utilise la **fonction Excel12** pour sélectionner la cellule à partir de laquelle elle a été appelée.
  
Cet exemple de code fait partie d’un exemple plus large fourni dans le SDK XLL Excel 2010, à l’emplacement suivant où vous avez installé le SDK :
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Cette fonction appelle une macro de commande (xlcSelect) et, par conséquent, ne fonctionne que si elle est appelée à partir d’une feuille macro XLM.
  
```cs
short WINAPI Excel12Example(void)
{
    XLOPER12 xRes;
    Excel12(xlfCaller, &xRes, 0);
    Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>Voir aussi

[Excel4v/Excel12v](excel4v-excel12v.md)

