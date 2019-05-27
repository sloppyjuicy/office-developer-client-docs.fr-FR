---
title: Gestion de la m�moire dans Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 memory [excel 2007],managing memory in Excel,Excel stack,strings [Excel 2007], managing memory,memory management in Excel,XLOPER memory [Excel 2007],memory [Excel 2007], management guidelines
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419540"
---
# <a name="memory-management-in-excel"></a>Gestion de la mémoire dans Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
La gestion de la mémoire est l’élément le plus important à prendre en compte pour créer des XLL efficaces et stables. Un échec de la gestion de la mémoire peut entraîner différents problèmes dans Microsoft Excel, des problèmes mineurs tels qu’une initialisation et une allocation de mémoire inefficaces, ainsi que de petites pertes de mémoire ou des problèmes plus importants tels que la déstabilisation d’Excel.
  
Une mauvaise gestion de la m�moire repr�sente la source la plus courante des probl�mes graves li�s aux compl�ments. Par cons�quent, vous devez g�n�rer votre projet avec une strat�gie de gestion de la m�moire coh�rente et bien �tudi�e. 
  
La gestion de la m�moire est devenue plus complexe dans Microsoft Office Excel�2007 avec l�introduction du recalcul de la feuille de calcul multithread. Si vous voulez cr�er et exporter des fonctions de feuille de calcul thread-safe, vous devez g�rer les conflits qui risquent de se produire lorsque plusieurs threads se disputent l�acc�s.
  
Certains �l�ments doivent �tre pris en compte au sujet de la m�moire pour les trois�types de structure de donn�es suivants�:
  
- **XLOPER** et **XLOPER12**
    
- Les cha�nes qui ne sont pas dans une structure **XLOPER** ni dans une structure **XLOPER12**
    
- Les tableaux **FP** et **FP12** 
    
## <a name="xloperxloper12-memory"></a>Mémoire XLOPER/XLOPER12

La structure de données **XLOPER**/ **XLOPER12** a plusieurs sous-types qui contiennent des pointeurs vers les blocs de mémoire, à savoir des chaînes (**xltypeStr**), des tableaux (**xltypeMulti**) et des références externes (**xltypeRef**). En outre, les tableaux **xltypeMulti** peuvent contenir des éléments **XLOPER**/ **XLOPER12** de chaîne qui pointent ensuite vers d’autres blocs de mémoire. 
  
Une structure **XLOPER**/ **XLOPER12** peut �tre cr��e de diff�rentes mani�res�: 
  
- Via Excel lors de la pr�paration des arguments � transmettre � une fonction XLL
    
- Via Excel lors du renvoi d�une structure **XLOPER** ou **XLOPER12** dans un appel d�API C 
    
- Via votre DLL lors de la cr�ation des arguments � transmettre � un appel d�API C
    
- Via votre DLL lors de la cr�ation d�une valeur de retour de la fonction XLL
    
Un bloc de m�moire dans l�un des types de pointage de m�moire peut �tre allou� de plusieurs fa�ons�:
  
- Il peut s�agir d�un bloc statique dans votre DLL, en dehors de tout code de fonction, auquel cas il est inutile d�allouer ou de lib�rer de la m�moire.
    
- Il peut s�agir d�un bloc statique dans votre DLL, dans du code de fonction, auquel cas il est inutile d�allouer ou de lib�rer de la m�moire.
    
- Il peut �tre allou� dynamiquement et lib�r� par votre DLL de plusieurs diff�rentes mani�res�: **malloc** et **free** **new** et **delete**, etc.
    
- Il peut �tre allou� dynamiquement par Excel.
    
�tant donn� le nombre d�origines possibles pour la m�moire **XLOPER**/ **XLOPER12** et le nombre de situations dans lesquelles cette m�moire peut avoir �t� affect�e � la structure **XLOPER**/ **XLOPER12**, il n�est pas surprenant que cet objet puisse sembler difficile. Toutefois, cette complexit� peut �tre consid�rablement r�duite si vous suivez plusieurs r�gles et recommandations. 
  
### <a name="rules-for-working-with-xloperxloper12"></a>Règles d’utilisation de XLOPER/XLOPER12

- Ne tentez pas de lib�rer de la m�moire ni de remplacer les structures **XLOPERs**/ **XLOPER12** transmises comme arguments vers votre fonction XLL. Vous devez consid�rer ces arguments comme �tant en lecture seule. Pour plus d�informations, consultez la rubrique � Renvoi de **XLOPER** ou **XLOPER12** par la modification des arguments actifs�� dans [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).
    
- Si Excel a allou� de la m�moire pour une structure **XLOPER**/ **XLOPER12** renvoy�e vers votre DLL dans un appel vers l�API C�: 
    
  - Vous devez lib�rer de la m�moire lorsque vous n�avez plus besoin de la structure **XLOPER**/ **XLOPER12** � l�aide d�un appel vers [xlFree](xlfree.md). N�utilisez aucune autre m�thode, de lib�ration ou de suppression par exemple, pour lib�rer de la m�moire.
    
  - Si le type renvoy� est **xltypeMulti**, ne remplacez aucune structure **XLOPER**/ **XLOPER12** dans le tableau, surtout si elles contiennent des cha�nes, et surtout � l�emplacement o� vous essayez de remplacer une cha�ne.
    
  - Si vous voulez renvoyer la structure **XLOPER**/ **XLOPER12** vers Excel en tant que valeur de retour de votre fonction DLL, vous devez indiquer � Excel qu�il doit lib�rer de la m�moire lorsque vous avez termin�. 
    
- Vous devez uniquement appeler **xlFree** sur une structure **XLOPER**/ **XLOPER12** qui a �t� cr��e en tant que valeur de retour vers un appel d�API C. 
    
- Si votre DLL a allou� de la m�moire pour une structure **XLOPER**/ **XLOPER12** que vous souhaitez renvoyer vers Excel en tant que valeur de retour de votre fonction DLL, vous devez indiquer � Excel que la DLL doit lib�rer de la m�moire. 
    
### <a name="guidelines-for-memory-management"></a>Instructions pour la gestion de la mémoire

- Soyez cohérent au sein de la DLL quant à la méthode que vous utilisez pour allouer et libérer de la mémoire. Évitez de mélanger différentes méthodes. Une bonne approche consiste à placer la méthode que vous utilisez dans une classe de mémoire ou une structure, dans laquelle vous pouvez modifier la méthode utilisée sans modifier votre code à de nombreux endroits.
    
- Lorsque vous cr�ez des tableaux **xltypeMulti** dans votre DLL, soyez coh�rent dans la m�thode utilis�e pour allouer de la m�moire pour les cha�nes�: allouez toujours la m�moire dynamiquement ou utilisez toujours la m�moire statique. Ainsi, lorsque vous lib�rez de la m�moire, vous savez si vous devez toujours, ou jamais, lib�rer les cha�nes. 
    
- Effectuez des copies compl�tes de la m�moire allou�e par Excel lorsque vous copiez une structure **XLOPER**/ **XLOPER12** cr��e dans Excel.
    
- Ne placez pas des structures **XLOPER**/ **XLOPER12** de chaîne allou�e par Excel dans des tableaux **xltypeMulti**. Effectuez une copie compl�te des chaînes et stockez des pointeurs vers les copies dans le tableau. 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Libérer de la mémoire XLOPER/XLOPER12 allouée par Excel

Utilisez la commande XLL, qui se sert de **xlGetName** pour obtenir une cha�ne contenant le chemin d�acc�s et le nom de fichier de la DLL, et qui affiche ces informations dans une bo�te de dialogue d�alerte � l�aide de **xlcAlert**.
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

Lorsque la fonction n�a plus besoin de la m�moire vers laquelle pointe **xDllName**, elle peut la lib�rer � l�aide d�un appel vers la [fonction xlFree](xlfree.md), l�une des fonctions d�API C pour DLL uniquement. 
  
La fonction **xlFree** est d�crite en d�tail dans la section des r�f�rences de fonction (voir [Fonctions de l�API�C qui peuvent �tre appel�es uniquement � partir d�une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), mais tenez compte des �l�ments suivants�:
  
- Vous pouvez transmettre les pointeurs vers plusieurs **XLOPER**/ **XLOPER12** dans un appel unique vers **xlFree**, la seule limite �tant le nombre d�arguments de fonction pris en charge dans la version d�Excel en cours d�ex�cution (30 dans Excel 2003, 255 � partir de Excel 2007).
    
- **xlFree** d�finit le pointeur contenu vers **NULL** pour s�assurer qu�une tentative de lib�ration d�une structure **XLOPER**/ **XLOPER12** qui a d�j� �t� lib�r�e est s�curis�e. **xlFree** est la seule fonction d�API C qui modifie ses arguments. 
    
- Vous pouvez appeler en toute s�curit� **xlFree** sur n�importe quelle structure **XLOPER**/ **XLOPER12** utilis�e pour la valeur de retour d�un appel de l�API C, ind�pendamment du fait qu�elle contienne ou non un pointeur vers la m�moire. 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Renvoi des XLOPER/XLOPER12 à libérer via Excel

Supposons que vous vouliez modifier l�exemple de commande dans la section pr�c�dente et la remplacer par une fonction de feuille de calcul qui renvoie le chemin d�acc�s et le nom de fichier de DLL lorsqu�un argument **Boolean** **true** est transmis, et **#N/A** dans le cas contraire. Vous ne pouvez clairement pas appeler **xlFree** pour lib�rer la m�moire de cha�ne avant son renvoi vers Excel. Toutefois, si elle n�est pas lib�r�e � un moment donn�, le compl�ment perd de la m�moire chaque fois que la fonction est appel�e. Pour contourner ce probl�me, vous pouvez d�finir un bit dans le champ **xltype** de la structure **XLOPER**/ **XLOPER12**, d�fini comme **xlbitXLFree** dans xlcall.h. Cela indique � Excel qu�il doit lib�rer la m�moire renvoy�e lorsqu�il a termin� la copie de la valeur. 
  
### <a name="example"></a>Exemple

L’exemple de code suivant illustre la commande XLL de la section précédente convertie en une fonction de feuille de calcul XLL.
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

Les fonctions XLL qui utilisent **XLOPER**/ **XLOPER12** doivent �tre d�clar�es comme prenant et renvoyant des pointeurs vers **XLOPER**/ **XLOPER12**. L�utilisation dans cet exemple d�une structure **XLOPER12** statique au sein de la fonction n�est pas thread-safe. Vous pouvez inscrire incorrectement cette fonction en tant que thread-safe, mais vous risqueriez de remplacer **xRtnValue** par un thread avant qu�un autre thread ne soit termin� pour cette fonction. 
  
Vous devez d�finir **xlbitXLFree** apr�s l�appel vers le rappel Excel qui l�alloue. Si vous le d�finissez avant, il est remplac� et n�a pas l�effet voulu. Si vous avez l�intention d�utiliser cette valeur comme un argument dans un appel vers une autre fonction d�API C avant de la renvoyer vers la feuille de calcul, vous devez d�finir ce bit apr�s un appel de ce type. Dans le cas contraire, vous confondrez les fonctions qui ne masquent pas ce bit avant de v�rifier le type de **XLOPER**/ **XLLOPER12**. 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>Renvoi des XLOPER/XLOPER12 à libérer via la DLL

Un probl�me semblable � celui-ci se produit lorsque votre XLL a allou� de la m�moire pour une structure **XLOPER**/ **XLOPER12** et souhaite la renvoyer vers Excel. Excel reconna�t un autre bit qui peut �tre d�fini dans le champ **xltype** de la structure **XLOPER**/ **XLOPER12**, d�fini comme **xlbitDLLFree** dans xlcall.h. 
  
Lorsqu�Excel re�oit **an XLOPER**/ **XLOPER12** avec ce bit d�fini, il essaie d�appeler une fonction qui doit �tre export�e par la XLL appel�e [xlAutoFree ](xlautofree-xlautofree12.md) (pour les **XLOPER**) ou **xlAutoFree12** (pour les **XLOPER12**). Cette fonction est d�crite plus en d�tail dans la r�f�rence de la fonction (voir [Gestionnaire de compl�ments et les fonctions de l'Interface XLL](add-in-manager-and-xll-interface-functions.md)), mais un exemple d�impl�mentation minimale est indiqu� ici. Son but est de lib�rer la m�moire **XLOPER**/ **XLOPER12** de fa�on coh�rente avec la mani�re dont elle a �t� allou�e � l�origine. 
  
### <a name="examples"></a>Exemples

L�exemple de fonction suivant a le m�me r�sultat que la fonction pr�c�dente, sauf qu�elle inclut le texte ��Le chemin d�acc�s complet de cette DLL est�� avant le nom de la DLL.
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

Une impl�mentation minimale suffisante de **xlAutoFree12** dans la XLL qui a export� la fonction pr�c�dente se pr�sente comme suit. 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

Cette impl�mentation est uniquement suffisante si la XLL renvoie uniquement des cha�nes **XLOPER12**, et que ces cha�nes sont uniquement allou�es � l�aide de **malloc**. Notez que le test 
  
 ` if(p_oper->xltype == xltypeStr) `
  
�chouerait dans ce cas car **xlbitDLLFree** est d�fini. 
  
En g�n�ral, **xlAutoFree** et **xlAutoFree12** doivent �tre impl�ment�s afin qu�ils lib�rent de la m�moire associ�e aux tableaux **xltypeMulti** cr��s via XLL et aux r�f�rences externes **xltypeRef**. 
  
Vous pouvez d�cider d�impl�menter vos fonctions XLL afin qu�elles renvoient toutes les structures **XLOPER** et **XLOPER12** allou�es dynamiquement. Dans ce cas, vous devez d�finir **xlbitDLLFree** sur toutes ces **XLOPER** et **XLOPER12**, ind�pendamment du sous-type. Vous devez �galement impl�menter **xlAutoFree** et **xlAutoFree12** afin que cette m�moire soit lib�r�e, ainsi que la m�moire qui est vis�e par le pointeur dans la structure **XLOPER**/ **XLOPER12**. Cette approche est une fa�on de garantir que la valeur de retour est thread-safe. Par exemple, la fonction pr�c�dente peut �tre r��crite comme suit.
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

Pour plus d�informations sur **xlAutoFree** et **xlAutoFree12**, consultez [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).
  
## <a name="returning-modify-in-place-arguments"></a>Renvoyer des arguments actifs à modifier

Excel permet à une fonction XLL de renvoyer une valeur en modifiant un argument actif. Ceci est possible uniquement avec un argument transmis en tant que pointeur. Pour cela, la fonction doit être inscrite dans une méthode qui indique à Excel l’argument qui sera modifié. 
  
Cette m�thode de renvoi d�une valeur est prise en charge pour tous les types de donn�es pouvant �tre transmis par le pointeur mais est particuli�rement utile pour les types suivants�:
  
- Cha�nes d�octets ASCII de longueur compt�e et se terminant par null
    
- Cha�nes de caract�res larges Unicode de longueur compt�e et se terminant par null (d�marrage dans Excel 2007)
    
- Tableaux **FP** � virgule flottante 
    
- Tableaux **FP12** � virgule flottante (d�marrage dans Excel 2007) 
    
> [!NOTE]
> [!REMARQUE] Vous ne devriez pas essayer de renvoyer des **XLOPER** ou des **XLOPER12** de telle mani�re. Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md). 
  
L�avantage de cette technique, plut�t que d�utiliser simplement l�instruction de renvoi, est qu�Excel alloue la m�moire pour les valeurs de retour. Une fois qu�Excel a fini de lire les donn�es renvoy�es, il lib�re la m�moire. Cela place les t�ches de gestion de la m�moire en dehors de la fonction XLL. Cette technique est thread-safe�: si elle est appel�e simultan�ment par Excel sur diff�rents threads, chaque appel de fonction sur chaque thread poss�de sa propre m�moire tampon.
  
Cette technique est utile en particulier pour les types de donn�es r�pertori�es, car le m�canisme de rappel dans la DLL pour lib�rer de la m�moire apr�s le renvoi qui existe pour **XLOPER**/ **XLOPER12** n�existe pas pour les cha�nes simples ni pour les tableaux **FP**/ **FP12**. Par cons�quent, lors du renvoi d�une cha�ne cr��e par la DLL ou un tableau � virgule flottante, les choix suivants s�offrent � vous�: 
  
- D�finissez un pointeur permanent vers une m�moire tampon allou�e dynamiquement, renvoyez le pointeur. Lors du prochain appel vers la fonction, (1) v�rifiez que le pointeur n�est pas null, (2) lib�rez les ressources allou�es � l�appel pr�c�dent et r�tablissez le pointeur sur null, et (3) r�utilisez le pointeur pour un bloc de m�moire nouvellement allou�.
    
- Cr�ez des cha�nes et des tableaux dans une m�moire tampon statique ne n�cessitant pas d��tre lib�r�e et renvoyez un pointeur vers celle-ci.
    
- Modifiez un argument actif, �crivez votre cha�ne ou votre tableau directement dans l�espace utilis� par Excel.
    
Dans le cas contraire, vous devez cr�er une structure **XLOPER**/ **XLOPER12** et utiliser **xlbitDLLFree** et **xlAutoFree**/ **xlAutoFree12** pour lib�rer les ressources. 
  
La derni�re option est peut-�tre la plus simple lorsque vous transmettez un argument du m�me type que la valeur de retour. Le point essentiel � retenir est le suivant : les tailles de m�moire tampon sont limit�es et vous devez veiller � ne pas les saturer. Le non-respect de cette consigne peut entra�ner une panne d�Excel. Les tailles de la m�moire tampon pour les chaînes et les tableaux **FP**/ **FP12** sont trait�es plus loin. 
  
## <a name="strings"></a>Strings

Les problèmes liés à la gestion de la mémoire de chaîne sont sans doute la cause la plus courante d’instabilité dans les applications et les compléments. Cela peut être compréhensible, étant donné les diverses manières selon lesquelles les chaînes sont traitées : terminées par null ou de longueur comptée (ou les deux) ; mémoires tampons statiques ou dynamiques ; longueur fixe ou longueur presque illimitée ; mémoire gérée par le système d’exploitation (par exemple, OLE Bstr) ou chaînes non gérées ; etc.
  
Les programmeurs C/C++ rencontrent souvent des cha�nes termin�es par null. La biblioth�que C standard est con�ue pour fonctionner avec ce type de cha�ne. Les litt�raux de cha�ne statique dans le code sont compil�s dans des cha�nes termin�es par null. Sinon, Excel fonctionne avec des cha�nes de longueur compt�e qui en g�n�ral ne sont pas termin�es par null. La combinaison de ces aspects requiert une approche claire et coh�rente dans votre DLL/XLL concernant la mani�re dont vous g�rez les cha�nes et la m�moire de cha�ne.
  
Les probl�mes les plus courants sont les suivants�:
  
- La transmission d�un pointeur null ou non valide vers une fonction qui attend un pointeur valide et qui ne v�rifie pas ou ne peut pas v�rifier la validit� du pointeur elle-m�me.
    
- Le d�passement des limites d�une m�moire tampon de cha�ne par une fonction qui ne v�rifie pas ou ne peut pas v�rifier la longueur de la m�moire tampon par rapport � la longueur de la cha�ne en cours d��criture.
    
- Une tentative de lib�ration de la m�moire tampon de cha�ne qui est statique, qui a d�j� �t� lib�r�e ou qui n��tait pas allou�e de fa�on coh�rente avec la mani�re dont elle est lib�r�e.
    
- Des pertes de mémoire résultant de chaînes allouées et non libérées, généralement dans une fonction fréquemment appelée.
    
### <a name="rules-for-strings"></a>Règles pour les chaînes

Comme pour les structures **XLOPER**/ **XLOPER**, il existe des r�gles et des instructions � suivre. Les instructions sont les m�mes que celles �num�r�es dans la section pr�c�dente. Les r�gles d�crites ici sont une extension des r�gles propres aux chaînes.
  
 **R�gles�:**
  
- Ne tentez pas de lib�rer de la m�moire ou de remplacer une cha�ne **XLOPER**/ **XLOPER12** ou des cha�nes de longueur compt�e ou termin�es par null transmises comme arguments � la fonction de votre XLL. Vous devez consid�rer ces arguments comme �tant en lecture seule.
    
- Lorsque Excel alloue de la m�moire � une cha�ne **XLOPER**/ **XLOPER12** pour la valeur de retour d�une fonction de rappel API C, utilisez **xlFree** pour la lib�rer ou d�finissez **xlbitXLFree** si vous la renvoyez vers Excel � partir d�une fonction XLL. 
    
- Lorsque votre DLL alloue dynamiquement une m�moire tampon de cha�ne pour une structure **XLOPER**/ **XLOPER12**, lib�rez-la de fa�on coh�rente avec la mani�re dont vous l�allouez une fois que vous avez termin� ou d�finissez **xlbitDLLFree** si vous la renvoyez vers Excel � partir d�une fonction XLL, puis lib�rez-la dans **xlAutoFree**/ **xlAutoFree12**.
    
- Si Excel a allou� la m�moire pour un tableau **xltypeMulti** renvoy� � votre DLL dans un appel d�API C, ne remplacez aucune cha�ne **XLOPER**/ **XLOPER12** dans le tableau. Ces tableaux doivent uniquement �tre lib�r�s � l�aide de **xlFree**, ou en cas de renvoi par une fonction XLL, par la d�finition de **xlbitXLFree**.
    
### <a name="string-types-supported"></a>Types de chaîne pris en charge

**API C xltypeStr XLOPER/XLOPER12s**

|**Cha�nes d�octets�: **XLOPER****|**Cha�nes de caract�res larges�: **XLOPER12****|
|:-----|:-----|
|Toutes les versions d�Excel  <br/> |D�marrage dans Excel 2007  <br/> |
|Longueur maximale�: 255�octets ASCII �tendus  <br/> |Longueur maximale�: 32�767 caract�res Unicode  <br/> |
|Le premier octet (non sign�) = longueur  <br/> |Le premier caract�re Unicode = longueur  <br/> |
   
> [!IMPORTANT]
> [!IMPORTANTE] Ne supposez pas que les cha�nes **XLOPER** ou **XLOPER12** se terminent par null. 
  
**Cha�nes C/C++**

|**Cha�nes d�octets**|**Chaînes de caractères larges**|
|:-----|:-----|
|Longueur maximale de l’élément « C » terminé par null (**char** *) : 255 octets ASCII étendus  <br/> |Longueur maximale de l’élément « C% » terminé par null (**wchar_t** *) : 32 767 caractères Unicode  <br/> |
|Longueur comptée (**char non signé** *) : « D »  <br/> |Longueur comptée ((**wchar_t** *) *) : « D % »  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>Chaînes dans les tableaux xltypeMulti XLOPER/XLOPER12

Dans certains cas, Excel cr�e un tableau **xltypeMulti** � utiliser dans votre DLL/XLL. Plusieurs fonctions d�informations XLM renvoient ces tableaux. Par exemple, la fonction de l�API C **xlfGetWorkspace**, lorsque l�argument  *44*  est transmis, renvoie un tableau contenant des chaînes qui d�crivent toutes les proc�dures DLL actuellement inscrites. La fonction de l�API C **xlfDialogBox** renvoie une copie modifi�e de l�argument de tableau, contenant des copies compl�tes des chaînes. Une XLL rencontre peut-�tre le plus couramment un tableau **xltypeMulti** � l�endroit o� il a �t� transmis en tant qu�argument vers une fonction XLL, ou l� o� il a �t� converti en ce type � partir d�une r�f�rence de plage. Dans ce dernier cas, Excel cr�e des copies compl�tes des chaînes dans les cellules sources et pointe vers celles-ci dans le tableau. 
  
� l�endroit o� vous souhaitez modifier ces cha�nes dans votre DLL, vous devez effectuer vos propres copies compl�tes. Lorsque vous cr�ez vos propres tableaux **xltypeMulti**, vous ne devez pas placer la cha�ne allou�e par Excel **XLOPER**/ **XLOPER12**. Vous risquez ainsi de ne pas les lib�rer correctement ult�rieurement, ou de ne pas les lib�rer du tout. L� encore, vous devez effectuer des copies compl�tes des cha�nes et stocker des pointeurs vers les copies dans le tableau.
  
 **Exemples**
  
La fonction de l�exemple suivant cr�e une copie d�une cha�ne Unicode de longueur compt�e allou�e dynamiquement. Notez que l�appelant doit finalement lib�rer la m�moire allou�e dans cet exemple � l�aide de **delete**[], et que la cha�ne source n�est pas suppos�e se terminer par null. La cha�ne de copie est tronqu�e si n�cessaire pour des raisons de s�curit� et ne se termine pas par null.
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

Cette fonction peut ensuite �tre utilis�e en toute s�curit� pour copier une structure **XLOPER12**, comme indiqu� dans la fonction XLL exportable suivante qui renvoie une copie de l�argument s�il s�agit d�une chaîne. Tous les autres types sont renvoy�s comme une chaîne de longueur nulle. Notez que si les plages ne sont pas g�r�es, la fonction renvoie **#VALUE!**. La fonction doit �tre inscrite comme prenant un argument de type U afin que les r�f�rences soient transmises en tant que valeurs. Cela �quivaut � la fonction de feuille de calcul int�gr�e **T()**, sauf que **AsText** convertit �galement les erreurs en chaînes de longueur nulle. Cet exemple de code suppose que **xlAutoFree12** lib�re le pointeur transmis, ainsi que son contenu, � l�aide de **delete**.
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a>Renvoi d’arguments de chaîne actifs à modifier

Les arguments inscrits en tant que types **F**, **G**, **F%** et **G%** peuvent �tre modifi�s en actifs. Quand Excel pr�pare les arguments de cha�ne pour ces types, il cr�e une m�moire tampon de longueur maximale. Il copie ensuite la cha�ne d�argument dans celle-ci, m�me si cette cha�ne est beaucoup plus courte. Ainsi, la fonction XLL peut �crire sa valeur de retour directement dans la m�me m�moire. 
  
Les diff�rentes tailles de m�moire tampon pour ces types sont les suivantes�:
  
- **Cha�nes d�octets�:** 256�octets, y compris de longueur compt�e (type G) ou termin�es par null (type F). 
    
- **Cha�nes Unicode�:** 32�768 caract�res larges (65�536 octets), y compris de longueur compt�e (type G�%) ou termin�es par null (type F�%). 
    
> [!NOTE]
> [!REMARQUE] Vous ne pouvez pas appeler une telle fonction directement � partir de Visual Basic pour Applications (VBA), car vous ne pouvez pas garantir qu�une m�moire tampon suffisamment large a �t� affect�e. Vous pouvez uniquement appeler une telle fonction � partir d�une autre DLL en toute s�curit� si vous avez explicitement transmis une m�moire tampon suffisamment large. 
  
Voici un exemple d�une fonction XLL qui annule une cha�ne de caract�res larges termin�e par null transmise � l�aide de la fonction de biblioth�que standard **wcsrev**. Dans ce cas, l�argument peut �tre inscrit en tant que type **F%**.
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>Stockage permanent (noms binaires)

Les noms binaires sont d�finis et associ�s � des blocs de donn�es binaires, autrement dit, non structur�es, qui sont stock�es avec la feuille de calcul. Ils sont cr��s � l�aide de la fonction [xlDefineBinaryName ](xldefinebinaryname.md) et les donn�es sont r�cup�r�es � l�aide de la fonction [xlGetBinaryName ](xlgetbinaryname.md). Les deux fonctions sont d�crites plus en d�tail dans la r�f�rence de la fonction (voir [Fonctions de l�API C qui peuvent �tre appel�es uniquement � partir d�une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)) et utilisent **xltypeBigData** **XLOPER**/ **XLOPER12**. 
  
Pour plus d�informations sur les probl�mes connus qui limitent les applications pratiques des noms binaires, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).
  
## <a name="excel-stack"></a>Pile d’Excel

Excel partage son espace de pile avec toutes les DLL chargées. L’espace de pile est généralement plus adapté à une utilisation ordinaire, et il est inutile de vous préoccuper tant que vous respectez les instructions suivantes : 
  
- Ne transmettez pas de tr�s grandes structures comme des arguments vers des fonctions par valeur sur la pile. Transmettez plut�t des pointeurs ou des r�f�rences.
    
- Ne renvoyez pas de grandes structures sur la pile. Renvoyez des pointeurs vers la m�moire allou�e de mani�re dynamique ou statique, ou utilisez les arguments transmis par r�f�rence.
    
- Ne d�clarez pas de tr�s grandes structures variables automatiques dans le code de la fonction. Si vous en avez besoin, d�clarez-les comme �tant statiques.
    
- N�appelez pas les fonctions de mani�re r�cursive, sauf si vous �tes s�r que la profondeur de r�cursivit� sera toujours faible. Essayez plut�t d�utiliser une boucle.
    
Lorsqu�une DLL rappelle dans Excel � l�aide d�une API C, Excel v�rifie d�abord s�il y a suffisamment d�espace sur la pile pour l�appel d�utilisation le plus d�favorable pouvant �tre effectu�. S�il pense que l�espace est insuffisant, il fait �chouer l�appel pour des raisons de s�curit�, bien que l�espace puisse �tre suffisant pour cet appel en particulier. Dans ce cas, les rappels renvoient le code **xlretFailed**. Pour une utilisation ordinaire de l�API C et de la pile, il s�agit d�une cause d��chec d�un appel d�API C peu probable.
  
Si cela vous pr�occupe, si vous �tes simplement curieux ou si vous souhaitez �liminer le manque d�espace de pile comme raison d�un �chec inexpliqu�, vous pouvez conna�tre la quantit� d�espace de pile disponible par un appel de la fonction [xlStack](xlstack.md). 
  
## <a name="see-also"></a>Voir aussi



[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
  
[Le multithreading et la Contention de m�moire dans Excel](multithreading-and-memory-contention-in-excel.md)
  
[Développement de XLL de Excel](developing-excel-xlls.md)

