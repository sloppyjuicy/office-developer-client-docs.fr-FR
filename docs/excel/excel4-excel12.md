---
title: Excel4/Excel12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12
- Excel4
keywords:
- fonction Excel4 [Excel 2007], fonction Excel12 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7c3af5f380ae4144890b1f7b486a61a05c19de74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304108"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction de feuille de calcul Microsoft Excel interne, une fonction de feuille de macro ou une commande, ou une fonction ou une commande spéciale XLL uniquement, à partir d'une ressource DLL/XLL ou d'une ressource de code.
  
Toutes les versions récentes d'Excel prennent en charge **Excel4**. À partir d'Excel 2007, **Excel12** est pris en charge. 
  
Ces fonctions ne peuvent être appelées que lorsqu'Excel a passé le contrôle à la DLL ou au XLL. Elles peuvent également être appelées lorsqu'Excel a passé le contrôle indirectement via un appel à Visual Basic pour applications (VBA). Elles ne peuvent pas être appelées à un autre moment. Par exemple, ils ne peuvent pas être appelés pendant les appels à la fonction [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) ou à d'autres moments où le système d'exploitation a appelé la dll ou à partir d'un thread créé par la dll. 
  
Les fonctions [Excel4v et Excel12v](excel4v-excel12v.md) acceptent leurs arguments sous forme de tableau, tandis que les fonctions **Excel4** et **Excel12** acceptent leurs arguments sous la forme d'une liste de longueur variable sur la pile. À tous les autres égards, **Excel4** se comporte de la même manière que **Excel4v**, et **Excel12** se comporte de la même manière que **Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Paramètres

 _IFunction_ (**int**)
  
Nombre qui indique la commande, la fonction ou la fonction spéciale que vous souhaitez appeler. Pour obtenir la liste des valeurs _IFunction_ valides, reportez-vous à la section notes suivantes. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Pointeur vers un **XLOPER** (avec **Excel4**) ou un **XLOPER12** (avec **Excel12**) qui contiendra le résultat de la fonction évaluée.
  
 _iCount_ (**int**)
  
Nombre d'arguments suivants qui seront transmis à la fonction. Dans les versions d'Excel jusqu'à 2003, il peut s'agir d'un nombre compris entre 0 et 30. À partir d'Excel 2007, il peut s'agir de n'importe quel nombre compris entre 0 et 255.
  
 _argument1,..._ (**LPXLOPER** ou **LPXLOPER12**)
  
Arguments facultatifs de la fonction. Tous les arguments doivent être des pointeurs vers des valeurs **XLOPER** ou **XLOPER12** . 
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie l'une des valeurs entières (**int**) suivantes.
  
|**Valeur**|**Code de retour**|**Description**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |La fonction a été appelée avec succès. Cela ne signifie pas que la fonction n'a pas renvoyé une valeur d'erreur Excel; pour le savoir, vous devez examiner le type et la valeur du paramètre _pxRes_ résultant.  <br/> |
|0,1  <br/> |**xlretAbort** <br/> |La commande ou la fonction a été arrêtée de manière anormale (abandon interne). Cela peut se produire si une feuille macro XLM se ferme elle-même en appelant **Close**ou si la mémoire d'Excel est insuffisante. Si Excel renvoie cette erreur, la fonction d'appel doit se fermer immédiatement. La DLL est autorisée à appeler **xlFree** uniquement avant de quitter. Tous les autres appels à l'API C ne sont pas autorisés. L'utilisateur peut enregistrer les tâches interactives à l'aide de la commande **Enregistrer** du menu **fichier** .  <br/> |
|n°2  <br/> |**xlretInvXlfn** <br/> |Un numéro de fonction non valide a été fourni. Si vous utilisez des constantes à partir du fichier d'en-tête xlcall. h, cela ne doit pas se produire sauf si vous appelez un composant qui n'est pas pris en charge dans la version d'Excel que vous exécutez.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Un nombre d'arguments non valide a été entré. Dans les versions antérieures à Excel 2003, le nombre maximal d'arguments qu'une fonction peut prendre est de 30. À partir d'Excel 2007, le nombre maximal est 255. Certains nécessitent un nombre d'arguments fixe ou minimal.  <br/> |
|8bits  <br/> |**xlretInvXloper** <br/> |Une structure **XLOPER** ou **XLOPER12** non valide a été transmise à la fonction ou un argument de type incorrect a été utilisé.  <br/> |
|Seiz  <br/> |**xlretStackOvfl** <br/> |Un dépassement de capacité de la pile s'est produit. Utilisez **xlStack** pour contrôler la quantité d'espace restant sur la pile. Évitez d'allouer des tableaux et des structures très volumineux (automatiques) dans la pile, si possible; rendez-les statiques. (Notez qu'un dépassement de capacité de la pile peut se produire sans être détecté.)  <br/> |
|32  <br/> |**xlretFailed** <br/> |Une fonction équivalente à la commande a échoué. Cela équivaut à une commande de macro affichant la boîte de dialogue d'alerte d'erreur de macro.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Une tentative a été effectuée pour déréférencer une cellule qui n'a pas encore été calculée, car elle est planifiée pour être recalculée après la cellule active. Dans ce cas, la DLL doit renvoyer immédiatement le contrôle à Excel. La DLL est autorisée à appeler **xlFree** uniquement avant de quitter. Tous les autres appels à l'API C ne sont pas autorisés. Pour plus d'informations sur les fonctions qui peuvent et ne peuvent pas accéder aux valeurs des cellules qui n'ont pas été recalculées, voir [commandes, fonctions et États d'Excel](excel-commands-functions-and-states.md).  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Il y a eu une tentative d'appel d'une fonction qui n'est pas ou non thread-safe pendant un recalcul multithread du classeur.  <br/> À partir d'Excel 2007, cette valeur est renvoyée et uniquement dans les fonctions de feuille de calcul XLL déclarées comme thread-safe.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |Le descripteur de fonction asynchrone n'est pas valide.  <br/> Cette valeur est utilisée uniquement par Excel 2010.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |L'appel n'est pas pris en charge sur les clusters.  <br/> Cette valeur est utilisée uniquement par Excel 2010.  <br/> |
   
## <a name="remarks"></a>Remarques

### <a name="valid-ifunction-values"></a>Valeurs iFunction valides

Les valeurs **IFunction** valides sont l'une des constantes **XLF...** ou **XLC...** définies dans le fichier d'en-tête xlcall. h ou l'une des fonctions spéciales suivantes. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Différents types de fonctions

 **Excel4** et **Excel12** font la différence entre trois classes de fonctions. Les fonctions sont classées selon les trois États dans lesquels Excel peut appeler la DLL. 
  
- La classe 1 s'applique lorsque la DLL est appelée à partir d'une feuille de calcul suite à un recalcul. 
    
- La classe 2 s'applique lorsque la DLL est appelée à partir d'une macro de fonction ou d'une feuille de calcul dans laquelle elle a été enregistrée avec un signe dièse (#) dans le texte type.
    
- La classe 3 s'applique lorsqu'une DLL est appelée à partir d'un objet, d'une macro, d'un menu, d'une barre d'outils, d'une touche de raccourci, d'une méthode **ExecuteExcel4Macro,** ou de la commande **Outils/macro/exécuter** . Pour plus d'informations, consultez la rubrique [commandes, fonctions et États d'Excel](excel-commands-functions-and-states.md).
    
Le tableau suivant indique les fonctions qui sont valides dans chaque classe.
  
|**Classe 1**|**Classe 2**|**Classe 3**|
|:-----|:-----|:-----|
|N'importe quelle fonction de feuille de calcul  <br/> N'importe quelle fonction XLL-uniquement **XL...** sauf **xlSet**.  <br/> **xlfCaller** <br/> |N'importe quelle fonction de feuille de calcul  <br/> N'importe quelle fonction **XL...** sauf **xlSet**.  <br/> Fonctions de feuille macro, y compris **xlfCaller**, qui renvoient une valeur, mais qui n'effectue aucune action qui affecte l'objet Workspace ou un classeur ouvert.  <br/> |N'importe quelle fonction, y compris **xlSet** et les fonctions équivalentes à commande.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Affichage de la boîte de dialogue pour une fonction équivalente à une commande

Si une fonction équivalente à une commande est associée à une boîte de dialogue, vous pouvez définir le bit **xlPrompt** dans **IFunction**. Cela signifie qu'Excel affiche la boîte de dialogue appropriée avant d'exécuter la commande.
  
### <a name="writing-international-dlls"></a>Écriture de dll internationales

Si vous définissez le bit **xlIntl** dans **IFunction**, la fonction ou la commande est exécutée comme si elle était appelée à partir d'une feuille macro internationale. Cela signifie que la commande se comporte comme elle le ferait sur la version américaine d'Excel, même si elle s'exécute sur une version internationale (localisée).
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced ou xlretAbort

Après avoir reçu l'une de ces valeurs de retour, votre DLL doit nettoyer et retourner le contrôle à Excel immédiatement. Les rappels dans Excel via l'API C, à l'exception de **xlFree**, sont désactivés après la réception de l'une de ces valeurs de retour.
  
## <a name="example"></a>Exemple

L'exemple suivant utilise la fonction **Excel12** pour sélectionner la cellule à partir de laquelle elle a été appelée. 
  
Cet exemple de code fait partie d'un exemple plus complet fourni dans le kit de développement XLL Excel 2010, à l'emplacement suivant où vous avez installé le kit de développement logiciel (SDK):
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Cette fonction appelle une macro de commande (xlcSelect) et, par conséquent, fonctionne uniquement si elle est appelée à partir d'une feuille macro XLM. 
  
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

