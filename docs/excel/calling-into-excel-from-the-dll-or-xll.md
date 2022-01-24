---
title: Appel dans Excel à partir du fichier DLL ou XLL
manager: lindalu
ms.date: 01/22/2022
ms.audience: Developer
ms.topic: overview
keywords:
- dialog boxes [excel 2007], invoking excel commands,DLLs [Excel 2007], calling into Excel,passing arguments to C API functions [Excel 2007],commands [Excel 2007], invoking with dialog boxes,commands [Excel 2007], accessible from DLL/XLL,Excel4 function [Excel 2007],Excel12 function [Excel 2007],XLCallVer function [Excel 2007],operRes argument [Excel 2007],functions [Excel 2007], accessible from DLL/XLL,Excel12v function [Excel 2007],DLL-only functions [Excel 2007],C API [Excel 2007], passing arguments,count argument [Excel 2007],commands [Excel 2007], calling in international versions,DLL-only commands [Excel 2007],international versions [Excel 2007], calling functions and commands,XLLs [Excel 2007], calling into Excel,Excel 4v function [Excel 2007],xlfn argument [Excel 2007],functions [Excel 2007], calling in international versions
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.localizationpriority: high
ms.openlocfilehash: cac045bb41c4cb6d726935434b2efd192da289bb
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180760"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a>Appel dans Excel à partir du fichier DLL ou XLL

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Microsoft Excel permet � votre DLL d�acc�der aux commandes Excel int�gr�es, aux fonctions de feuille de calcul et aux fonctions de feuille de macro. Ces derni�res sont disponibles � partir des commandes et fonctions DLL appel�es � partir de Visual Basic pour Applications (VBA) ou des commandes et fonctions XLL appel�es directement par Microsoft Excel.
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a>Fonctions Excel4, Excel4v, Excel12 et Excel12v

Excel permet � vos DLL d�acc�der aux commandes et fonctions au moyen des fonctions de rappel [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel 12](excel4-excel12.md) et [Excel12v](excel4v-excel12v.md).
  
Les fonctions **Excel4** et **Excel4v** ont �t� introduites dans Excel�4. Elles travaillent avec la structure de donn�es **XLOPER**. Excel 2007 a introduit deux nouvelles fonctions de rappel, **Excel12** et **Excel12v**, travaillant avec la structure de donn�es **XLOPER12**. Les fonctions **Excel4** et **Excel4v** sont export�es par la biblioth�que Xlcall32.lib, qui doit �tre incluse dans votre projet DLL ou XLL. **Excel12** et **Excel12v** sont inclus dans le fichier source C++ du SDK, Xlcall.cpp, devant �tre ins�r� dans votre projet si vous souhaitez acc�der aux fonctionnalit�s Excel � l�aide de structures **XLOPER12**.
  
Le code suivant repr�sente les prototypes pour ces quatre fonctions. Les trois premiers arguments sont identiques, sauf que le deuxi�me argument est un pointeur vers une **XLOPER** dans la premi�re paire et un pointeur vers une **XLOPER12** dans la seconde paire. La convention d�appel est **_cdecl** dans **Excel4** et **Excel12** pour autoriser les listes d�arguments de variable. Les points de suspension repr�sentent les valeurs **XLOPER** pour **Excel4** et les valeurs **XLOPER12** pour **Excel12**. Le nombre de pointeurs est �gal � la valeur du param�tre  _count_.
  
**Toutes les versions d�Excel**
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
**Introduit dans Excel 2007**
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
Pour que la DLL puisse appeler **Excel4**, **Excel4v**, **Excel12** ou **Excel12v**, Excel doit passer le contr�le � la DLL. Cela signifie que ces rappels d�API C peuvent �tre r�alis�s uniquement dans les sc�narios suivants :
  
- Depuis une commande XLL qu’Excel a appelée directement ou via VBA.

- Depuis une feuille de calcul XLL ou une fonction de feuille de macro qu’Excel a appelée directement ou via VBA.

Vous ne pouvez pas appeler l’API C Excel dans les scénarios suivants :
  
- � partir d�un �v�nement de systéme d�exploitation (par exemple, depuis la fonction [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain)).

- À partir d’un thread en arrière-plan créé par votre DLL.

### <a name="return-values"></a>Valeurs de retour

Ces quatre fonctions renvoient un nombre entier qui indique � l�appelant si la fonction ou la commande a �t� correctement appel�e. Les valeurs renvoy�es peuvent faire partie des valeurs suivantes :
  
|**Valeur renvoy�e**|**D�finie dans Xlcall.h comme**|**Description**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |La fonction ou la commande a �t� ex�cut�e comme il se doit. Cela ne signifie pas que l�ex�cution �tait sans erreur. Par exemple, **Excel4** peut renvoyer **xlretSuccess** lors de l�appel de la fonction **FIND**, m�me si elle est �valu�e � **#VALUE!**, car le texte recherch� est introuvable. Vous devez examiner le type et la valeur de **XLOPER/XLOPER12** renvoy�e lorsque cela est possible.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Une macro de commande a �t� arr�t�e par l�utilisateur en cliquant sur le bouton **ANNULER** ou en appuyant sur la touche �CHAP.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |La fonction ou le code de commande fourni n�est pas valide. Cette erreur peut se produire lorsque la fonction d�appel n�est pas autoris�e � appeler la fonction ou la commande. Par exemple, une fonction de feuille de calcul ne peut pas appeler une fonction d�information feuille macro ou une fonction de commande.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Le nombre d’arguments fourni n’est pas correct dans l’appel.  <br/> |
|8   <br/> |**xlretInvXloper** <br/> |Une ou plusieurs valeurs d�argument **XLOPER** ou **XLOPER12** ne sont pas correctement mises en forme ou remplies.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Excel a détecté un risque que l’opération dépasse sa pile d’appels et, par conséquent, ne puisse pas appeler la fonction.  <br/> |
|32  <br/> |**xlretFailed** <br/> |La commande ou la fonction a �chou� pour une raison qui n�est pas d�crite par une des autres valeurs de retour. Une op�ration qui n�cessite trop de m�moire, par exemple, �choue avec l�erreur suivante. Cela peut se produire pendant la tentative de conversion d�une référence tr�s volumineuse � un tableau **xltypeMulti** � l�aide de la fonction [xlCoerce](xlcoerce.md).  <br/> |
|64  <br/> |**xlretUncalced** <br/> |L�op�ration a tent� de r�cup�rer la valeur d�une cellule non calcul�e. Pour pr�server l�int�grit� de recalcul dans Excel, les fonctions de feuille de calcul ne sont pas autoris�es � effectuer cette action. Toutefois, les fonctions et commandes XLL enregistr�es en tant que fonctions macro sont autoris�es � acc�der aux valeurs des cellules non calcul�es.  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |(Introduit dans Excel 2007) Une fonction de feuille de calcul XLL enregistr�e en tant que fonction thread-safe essayait d�appeler une fonction d�API C non thread-safe. Par exemple, une fonction thread-safe ne peut pas appeler la fonction XLM **xlfGetCell**.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |(Introduit dans Excel 2010) Le pointeur de fonction asynchrone n�est pas valide.  <br/> |
|512  <br/> |**xlretNotClusterSafe** <br/> |(Introduit dans Excel 2010) L�appel n�est pas pris en charge sur les clusters.  <br/> |
   
Si la fonction renvoie une des valeurs d��chec de la table (autrement dit, elle ne renvoie pas **xlretSuccess**), la valeur de retour **XLOPER** ou **XLOPER12** est �galement d�finie sur **#VALUE!**. Dans certains cas, il peut s�agir d�un test de r�ussite suffisant, mais vous remarquerez qu�un appel peut renvoyer � la fois **xlretSuccess** et **#VALUE!**.
  
Si un appel de l�API C entra�ne **xlretUncalced** ou **xlretAbort**, votre code DLL ou XLL doit rendre la main � Excel avant d�effectuer les autres appels d�API C (autres que les appels vers la fonction [xlfree](xlfree.md) pour lib�rer des ressources m�moire Excel allou�es dans les valeurs **XLOPER** et **XLOPER12**).
  
### <a name="command-or-function-enumeration-argument-xlfn"></a>Argument d’énumération de commande ou de fonction : xlfn

L�argument  _xlfn_ est le premier argument des fonctions de rappel et est un entier sign� 32�bits. Sa valeur doit �tre une des �num�rations de fonction ou de commande d�finies dans le fichier d�en-t�te SDK Xlcall.h, comme indiqu� dans l�exemple suivant. 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

Toutes les fonctions de feuille de calcul et de feuille de macro figurent dans la plage hexadécimale entre 0 (**xlfCount**) et 0x0fff bien que la valeur la plus élevée affectée dans Excel 2013 soit 547 (en base décimale) ou 0x0223 (en base hexadécimale). (**xlfFloor_precise**).
  
Toutes les fonctions de commande figurent dans la plage de nombres décimaux entre 0x8000 (**xlcBeep**) et 0x8fff, bien que la valeur la plus élevée affectée dans Excel 2013 soit 0x8328 (**xlcHideallInkannots**). EIles sont définis dans le fichier d'en-tête en tant que `(n | xlCommand)` où `n` est un nombre décimal supérieur ou égal à 0 et **xlCommand** est défini en tant que 0x8000 hexadécimal.
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a>Appel de commandes Excel qui utilisent des boîtes de dialogue

Certains codes de commande correspondent aux actions Excel qui utilisent des boîtes de dialogue. Par exemple, **xlcFileDelete** prend un seul argument : un nom de fichier ou un masque. Cet appel peut s’effectuer avec la boîte de dialogue afin que l’utilisateur puisse annuler ou modifier l’opération de suppression. Il peut s’effectuer également sans la boîte de dialogue, auquel cas le ou les fichiers sont supprimés sans autre intervention, en supposant qu’ils existent et que l’appelant dispose des autorisations nécessaires. Pour appeler de telles commandes dans leur formulaire de boîte de dialogue, l’énumération de commande doit être combinée à l’aide de l’opération OR avec 0x1000 (**xlPrompt**).
  
L�exemple suivant supprime les fichiers dans le r�pertoire actif correspondant au masque my_data\*.bak. Une bo�te de dialogue s�affiche uniquement si l�argument est vrai.
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a>Appel de fonctions et de commandes dans les versions internationales

Vous pouvez configurer Excel de façon à afficher les fonctions et les noms des commandes XML dans plusieurs langues. Certaines fonctions et commandes de l’API C opèrent sur des chaînes qui sont considérées comme des noms de fonction ou de commande. Par exemple, **xlcFormula** prend un argument de chaîne qui est destiné à être placé dans une cellule spécifiée. Pour que votre complément fonctionne avec tous les paramètres de langue, vous pouvez fournir les noms de chaîne en anglais et définir le bit 0x2000 (**xlIntl**) dans l’énumération de fonction ou de commande.
  
L'exemple de code suivant place l'équivalent de `=SUM(X1:X100)` dans la cellule A2 de la feuille active. Notez qu'il utilise la fonction Framework, **TempActiveRef**, pour créer une référence externe temporaire **XLOPER**. La formule apparaîtra dans la cellule A2 dans la langue locale correcte (par exemple, `=SOMME(X1:X100)` si la langue est le français).
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> �tant donn� que le r�sultat de l�appel de **Excel12** n�est pas requis, z�ro (NULL) peut �tre pass� comme deuxi�me argument � la place de l�adresse de **xResult**. Ce point est abord� en d�tail dans la section suivante. 
  
### <a name="dll-only-functions-and-commands"></a>Fonctions et commandes DLL uniquement

Excel prend en charge un petit nombre de fonctions accessibles uniquement depuis une DLL ou une XLL. Elles sont définies dans le fichier d'en-tête en tant que `(n | xlSpecial)` où `n` est un nombre décimal supérieur ou égal à 0 et `xlSpecial` est défini en tant que 0x4000 en hexadécimal. Ces fonctions sont répertoriées dans le tableau suivant et documentées dans la [Référence des fonctions API](excel-xll-sdk-api-function-reference.md).
  
||||
|:-----|:-----|:-----|
|[xlFree](xlfree.md) <br/> |0 | xlSpecial  <br/> |Libère les ressources de mémoire allouées par Excel.  <br/> |
|[xlStack](xlstack.md) <br/> |1 | xlSpecial  <br/> |Renvoie l’espace libre dans la pile Excel.  <br/> |
|[xlCoerce](xlcoerce.md) <br/> |2 | xlSpecial  <br/> |Convertit les types **XLOPER** et **XLOPER12**  <br/> |
|[xlSet](xlset.md) <br/> |3 | xlSpecial  <br/> |Fournit une méthode rapide de définition des valeurs de cellule.  <br/> |
|[xlSheetId](xlsheetid.md) <br/> |4 | xlSpecial  <br/> |Obtient un nom de feuille de calcul à l’aide de son ID interne.  <br/> |
|[xlSheetNm](xlsheetnm.md) <br/> |5 | xlSpecial  <br/> |Obtient un ID interne de feuille de calcul à l’aide de son nom.  <br/> |
|[xlAbort](xlabort.md) <br/> |6  | xlSpecial  <br/> |V�rifie si l�utilisateur a cliqu� sur le bouton **ANNULER** ou a appuy� sur la touche �CHAP.  <br/> |
|[xlGetInst](xlgetinst.md) <br/> |7  | xlSpecial  <br/> |Obtient le pointeur d’instance Excel.  <br/> |
|[xlGetHwnd](xlgethwnd.md) <br/> |8  | xlSpecial  <br/> |Obtient le pointeur de fenêtre principale Excel.  <br/> |
|[xlGetName](xlgetname.md) <br/> |9  | xlSpecial  <br/> |Obtient le chemin d’accès et le nom de la DLL.  <br/> |
|[xlEnableXLMsgs](xlenablexlmsgs.md) <br/> |10 | xlSpecial  <br/> |Cette fonction est déconseillée et ne doit plus être appelée.  <br/> |
|[xlDisableXLMsgs](xldisablexlmsgs.md) <br/> |11 | xlSpecial  <br/> |Cette fonction est déconseillée et ne doit plus être appelée.  <br/> |
|[xlDefineBinaryName](xldefinebinaryname.md) <br/> |12  | xlSpecial  <br/> |Définit un nom de stockage binaire permanent.  <br/> |
|[xlGetBinaryName](xlgetbinaryname.md) <br/> |13 | xlSpecial  <br/> |Obtient les données d’un nom de stockage permanent binaire.  <br/> |

## <a name="return-value-xloperxloper12-operres"></a>Renvoyer la valeur XLOPER/XLOPER12 : operRes

L’argument _operRes_ est le deuxième argument pour les rappels et il s’agit d’un pointeur vers un **XLOPER** (**Excel4** et **Excel4v**) ou **XLOPER12** (**Excel12** et **Excel12v**). Après un appel réussi, il contient la valeur de retour de la fonction ou de la commande. **operRes** peut être configuré sur zéro (pointeur NULL) si aucune valeur de retour n’est requise. Le contenu précédent de **operRes** est remplacé afin que toute mémoire précédemment pointée soit libérée avant l’appel pour éviter les pertes de mémoire.
  
Si la fonction ou la commande ne peut pas �tre appel�e (par exemple, si les arguments sont incorrects), **operRes** est d�finie sur l�erreur **#VALUE!**. Une commande retourne toujours **Boolean** **TRUE** si elle r�ussit, ou **FALSE** si elle a �chou� ou a �t� annul�e par l�utilisateur.
  
## <a name="number-of-subsequent-arguments-count"></a>Nombre d’arguments suivants

L�argument  _count_ est le troisi�me argument des rappels et est un entier sign� 32�bits. Il doit �tre configur� pour le nombre d�arguments suivants, en partant de 1. Si une fonction ou une commande ne prend aucun argument, elle doit �tre d�finie sur z�ro. Dans Microsoft Office Excel 2003, le nombre maximal d�arguments qu�une fonction accepte est �gal � 30 bien que la plupart des fonctions g�rent g�n�ralement moins d�arguments. � partir de Excel 2007, le nombre maximal d�arguments pouvant �tre pris en charge par une fonction est pass� � 255.
  
Avec **Excel4** et **Excel12**,  _count_ correspond au nombre de pointeurs vers les valeurs **XLOPER** ou **XLOPER12** transmises. Vous devez veiller � ne pas transmettre moins d�arguments que la valeur que  _count_ a d�finie. En effet, Excel risque d�effectuer des lectures anticip�es dans la pile et de tenter de lire des valeurs **XLOPER** ou **XLOPER12** non valides, ce qui pourrait bloquer l�application.
  
Avec **Excel4v** et **Excel12v**,  _count_ est la taille de la matrice des pointeurs vers les valeurs **XLOPER** ou **XLOPER12** transmises en tant qu�argument final. L� encore, vous devez veiller � ne pas passer un tableau inf�rieur �  _count_ �l�ments, car cela entra�nerait la saturation des limites de la matrice.
  
## <a name="passing-arguments-to-c-api-functions"></a>Passage d’arguments aux fonctions d’API C

**Excel4** et **Excel12** g�rent des listes d�arguments de longueur variable,  _count_, qui sont interpr�t�es comme des pointeurs vers les valeurs **XLOPER** et **XLOPER12**, respectivement. **Excel4v** et **Excel12v** g�rent un seul argument, apr�s  _count_, qui est un pointeur vers un tableau de pointeurs vers des valeurs **XLOPER** dans le cas de **Excel4v**, et vers des valeurs **XLOPER12** dans le cas de **Excel12v**.
  
Les formulaires de matrice **Excel4v** et **Excel12v** vous permettent de coder un appel � l�API C proprement lorsque le nombre d�arguments est variable. L�exemple suivant montre une fonction qui g�re un tableau de taille variable de nombres et qui utilise les fonctions de feuille de calcul Excel, via l�API C, pour calculer la somme, la moyenne, le minimum et le maximum.
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

Le remplacement des références des valeurs **XLOPER12** par **XLOPER**, et **Excel12v** par **Excel4v**, dans le code pr�c�dent permettait d�avoir une fonction compatible avec toutes les versions d�Excel. L�ex�cution de ces fonctions Excel **SUM**, **AVERAGE**, **MIN** et **MAX** est assez simple et il serait plus efficace de les coder en langage�C afin de ne pas avoir � pr�parer les arguments et l�appel dans Excel. Toutefois, la plupart des fonctions Excel sont plus complexes, ce qui rend cette approche utile dans certains cas.
  
La rubrique [xlfRegister](xlfregister-form-1.md) offre un autre exemple d�utilisation de **Excel4v** et **Excel12v**. Lorsque vous enregistrez une fonction de feuille de calcul XLL, vous pouvez fournir une cha�ne descriptive pour chaque argument utilis� dans la bo�te de dialogue **Coller une fonction**. Par cons�quent, le nombre total d�arguments fourni � **xlfRegister** d�pend du nombre d�arguments que votre fonction XLL accepte et varie d�une fonction � l�autre.
  
Lorsque vous appelez toujours une fonction API C ou une commande avec le m�me nombre d�arguments, vous voulez �viter d�avoir � cr�er un tableau de pointeurs pour ces arguments. Dans ce cas, il est plus simple et plus rationnel d�utiliser **Excel4** et **Excel12**. Par exemple, lorsque vous enregistrez des commandes et fonctions XLL, vous devez fournir le chemin et le nom de fichier complets de la DLL ou de la XLL. Vous pouvez obtenir le nom du fichier dans un appel � **xlfGetName**, puis le lib�rer avec un appel � **xlFree**, comme montr� dans l�exemple suivant pour **Excel4** et **Excel12**.
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

Dans la pratique, la fonction **Excel12v_example** peut �tre cod�e plus efficacement en cr�ant un seul argument **xltypeMulti** **XLOPER12** et en appelant l�API C � l�aide de **Excel12**, comme montr� dans l�exemple suivant.
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> Dans ce cas, la valeur de retour de **Excel12** est ignor�e. Au lieu de cela, le code v�rifie que le texte renvoy� **XLOPER12** est **xltypeNum** pour d�terminer si l�appel a r�ussi.
  
## <a name="xlcallver"></a>XLCallVer

Outre les rappels **Excel4**, **Excel4v**, **Excel12** et **Excel12v**, Excel exporte une fonction **XLCallVer**, qui retourne la version de l�API C en cours d�ex�cution.
  
La syntaxe du prototype de la fonction est la suivante :
  
 `int pascal XLCallVer(void);`
  
Vous pouvez appeler cette fonction thread-safe à partir de n’importe quelle commande ou fonction XLL.
  
D�Excel 97 � Excel 2003, **XLCallVer** renvoie 1280 = 0x0500 hex = 5 x 256, qui indique Excel�5. Depuis Excel 2007, elle renvoie 3072 = 0x0c00 hex = 12 x 256, qui indique de la m�me fa�on la version�12.
  
Bien que vous puissiez l'utiliser pour déterminer si la nouvelle API C est disponible au moment de l'exécution, vous préférerez peut-être détecter la version d'Excel en cours d'exécution en utilisant `Excel4(xlfGetWorkspace, &version, 1, &arg)`, où `arg` est un **XLOPER** numérique fixé à 2. La fonction renvoie une chaîne **XLOPER**, version, qui peut ensuite être convertie en un nombre entier. La raison pour laquelle on se base sur la version d'Excel plutôt que sur la version de l'API C est qu'il existe des différences entre Excel 2000, Excel 2002 et Excel 2003 que votre complément peut également devoir détecter. Par exemple, des modifications ont été apportées à la précision de certaines fonctions statistiques.
  
## <a name="see-also"></a>Voir aussi

- [Création de XLL](creating-xlls.md)  
- [Accés au code XLL dans Excel](accessing-xll-code-in-excel.md)  
- [Référence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)  
- [Les fonctions de rappel de l'API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)  
- [Développement de XLL de Excel 2013](developing-excel-xlls.md)
