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
- fonction Excel4 [excel 2007], fonction Excel12 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1c2c775cc7c5b051e4a1381df09ef29e79e2aca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782113"
---
# <a name="excel4excel12"></a>Excel4/Excel12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction de feuille de calcul Microsoft Excel interne, la fonction de feuille macro ou commande, ou XLL seule fonction spéciale ou, à partir d’au sein d’une DLL/XLL ou ressource de code.
  
Toutes les versions récentes d’Excel prennent en charge **Excel4**. À compter d’Excel 2007, **Excel12** est pris en charge. 
  
Ces fonctions peuvent être appelées uniquement lorsque Excel a réussi le contrôle à la DLL ou XLL. Ils peuvent également être appelées lorsque Excel a réussi le contrôle indirectement via un appel à Visual Basic pour Applications (VBA). Ils ne peuvent pas être appelées à tout moment. Par exemple, ils ne peut pas être appelées pendant un appel à la fonction [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) ou autres heures lorsque le système d’exploitation a appelé la DLL ou d’un thread créé par la DLL. 
  
Les fonctions [Excel4v et Excel12v](excel4v-excel12v.md) acceptent leurs arguments comme un tableau, tandis que les fonctions **Excel 4** et **Excel12** acceptent leurs arguments comme une liste de longueur variable sur la pile. Dans tous les autres aspects **Excel4** se comporte comme **Excel4v**et **Excel12** se comporte comme **Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Paramètres

 _iFunction_ (**int**)
  
Un nombre qui indique la commande, une fonction ou une fonction spéciale que vous voulez appeler. Pour obtenir la liste des valeurs valides _iFunction_ , voir la section Remarques suivante. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Pointeur vers un **XLOPER** (avec **Excel4**) ou une **XLOPER12** (avec **Excel12**) qui doit contenir le résultat de la fonction évaluée.
  
 _iCount_ (**int**)
  
Le nombre d’arguments suivants qui seront transmises à la fonction. Dans les versions d’Excel jusqu'à 2003, cela peut être n’importe quel nombre entre 0 et 30. À compter d’Excel 2007, il peut être n’importe quel nombre compris entre 0 et 255.
  
 _argument1..._ (**LPXLOPER** ou **LPXLOPER12**)
  
Les arguments facultatifs à la fonction. Tous les arguments doivent être des pointeurs vers les valeurs **XLOPER** ou **XLOPER12** . 
  
## <a name="return-value"></a>Valeur renvoy�e

Retourne l’une des valeurs suivantes entier (**int**).
  
|**Valeur**|**Code de retour**|**Description**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |La fonction a été appelée avec succès. Cela ne signifie pas que la fonction ne pas retourner une valeur d’erreur Excel ; Pour trouver des, vous devez examiner le type et la valeur du paramètre _pxRes_ qui en résulte.  <br/> |
|1  <br/> |**xlretAbort** <br/> |La commande ou la fonction a été interrompue anormalement (abandon interne). Cela peut se produire si une feuille de macro XLM se ferme en appelant **CLOSE**, ou si Excel est en dehors de la mémoire. Si Excel renvoie cette erreur, la fonction d’appel doit quitter immédiatement. La DLL est autorisée à appeler **xlFree** avant de quitter. Tous les autres appels à l’API C ne sont pas autorisés. L’utilisateur peut enregistrer tout travail de manière interactive à l’aide de la commande **Enregistrer** dans le menu **fichier** .  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |Un numéro de fonction non valide a été fourni. Si vous utilisez l’une des constantes à partir du fichier d’en-tête Xlcall.h, il doit se produit pas, sauf si vous appelez quelque chose qui n’est pas pris en charge dans la version d’Excel que vous exécutez.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Un nombre d’arguments non valide a été entré. Dans les versions jusqu'à Excel 2003, le nombre maximal de n’importe quelle fonction peut prendre des arguments est 30. À compter d’Excel 2007, le nombre maximal est 255. Certaines nécessitent un nombre fixe ou minimal d’arguments.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Une **XLOPER** ou **XLOPER12** non valide a été transmis à la fonction, ou un argument de type incorrect a été utilisé.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Un dépassement s’est produite. Utilisez **xlStack** pour surveiller la quantité d’espace libre sur la pile. Éviter l’allocation de très grands tableaux (automatiques) locales et les structures sur la pile lorsque cela est possible ; Rendre statique. (Notez qu’un dépassement peut se produire sans être détecté).  <br/> |
|32  <br/> |**xlretFailed** <br/> |Échec d’une fonction de l’équivalent de la commande. Cela équivaut à une commande de macro affichant la boîte de dialogue d’alerte macro.  <br/> |
|64  <br/> |**au niveau** <br/> |Une tentative a été effectuée pour supprimer la référence une cellule qui n’a pas encore été calculée, car elle est planifiée qui doit être recalculée après la cellule active. Dans ce cas, la DLL doit renvoyer contrôle vers Excel immédiatement. La DLL est autorisée à appeler **xlFree** avant de quitter. Tous les autres appels à l’API C ne sont pas autorisés. Pour plus d’informations sur les fonctions peuvent et ne peuvent pas accéder aux valeurs des cellules qui n’ont pas été recalculées, voir [Excel commandes, fonctions et états](excel-commands-functions-and-states.md).  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Une tentative a été effectuée pour appeler une fonction qui n’est pas, ou peut être pas thread-safe pendant un nouveau calcul multithread du classeur.  <br/> À compter d’Excel 2007, cette valeur est retournée, et uniquement dans les fonctions de feuille de calcul XLL déclarées en tant que thread-safe.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |La poignée de fonction asynchrone n’est pas valide.  <br/> Cette valeur est utilisée uniquement par Excel 2010.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |L’appel n’est pas pris en charge sur les clusters.  <br/> Cette valeur est utilisée uniquement par Excel 2010.  <br/> |
   
## <a name="remarks"></a>Remarques

### <a name="valid-ifunction-values"></a>Valeurs valides iFunction

Valeurs valides **iFunction** sont des constantes **xlf...** ou **xlc...** définis dans le fichier d’en-tête Xlcall.h ou une des fonctions spéciales suivantes. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Différents Types de fonctions

 **Excel4** et **Excel12** distinguer les trois classes de fonctions. Les fonctions sont classées en fonction des trois états dans lesquels Excel peut-être appeler la DLL. 
  
- Classe 1 s’applique lorsque la DLL est appelée à partir d’une feuille de calcul à la suite de recalcul. 
    
- Classe 2 s’applique lorsque la DLL est appelée à partir d’une macro de fonction ou d’une feuille de calcul dans laquelle il a été enregistré avec un signe dièse (#) dans le texte de type.
    
- Classe 3 s’applique lorsqu’une DLL est appelée à partir d’un objet, macro, menu, barre d’outils, touche de raccourci, méthode **ExecuteExcel4Macro** ou la commande **Macro/outils/exécuter** . Pour plus d’informations, voir [Excel commandes, fonctions et états](excel-commands-functions-and-states.md).
    
Le tableau suivant indique les fonctions qui sont valides dans chaque classe.
  
|**Classe 1**|**Classe 2**|**Classe 3**|
|:-----|:-----|:-----|
|Une fonction de feuille de calcul  <br/> Toutes les fonctions XLL seule **xl...** sauf **xlSet**.  <br/> **xlfCaller** <br/> |Une fonction de feuille de calcul  <br/> Une fonction **xl...** sauf **xlSet**.  <br/> Fonctions de feuille macro, y compris **xlfCaller**, qui renvoient une valeur sans effectuer aucune action qui affecte l’espace de travail ou un classeur ouvert.  <br/> |Une fonction, y compris **xlSet** et fonctions de l’équivalent de la commande.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Affichage de la boîte de dialogue pour une fonction équivaut à la commande

Si une fonction de l’équivalent de la commande a une boîte de dialogue associée, vous pouvez définir le bit **xlPrompt** dans **iFunction**. Cela signifie que Excel affiche la boîte de dialogue appropriée avant d’exécuter la commande.
  
### <a name="writing-international-dlls"></a>Écriture de DLL internationales

Si vous définissez le bit **xlIntl** dans **iFunction**, la fonction ou la commande s’effectue comme s’il a été appelée à partir d’une feuille de Macro internationale. Cela signifie que la commande se comporte comme sur la version d’Excel, même si elle s’exécute sur une version internationale (localisée).
  
### <a name="xlretuncalced-or-xlretabort"></a>au niveau ou xlretAbort

Après avoir reçu une de ces valeurs de retour, votre DLL doit nettoyer et retourne immédiatement le contrôle à Excel. Rappels dans Excel par le biais de l’API C, à l’exception **xlFree**, sont désactivées lorsqu’il reçoit une de ces valeurs de retour.
  
## <a name="example"></a>Exemple

L’exemple suivant utilise la fonction **Excel12** pour sélectionner la cellule à partir de laquelle il a été appelée. 
  
Cet exemple de code fait partie d’un exemple plus complet fourni dans le SDK XLL Excel 2010, à l’emplacement suivant, où vous avez installé le Kit de développement :
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Cette fonction appelle une macro de commande (xlcSelect) et, par conséquent, fonctionne uniquement si elle est appelée à partir d’une feuille de macro XLM. 
  
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

