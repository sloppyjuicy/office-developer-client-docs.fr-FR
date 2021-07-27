---
title: Compatibilité entre les versions 32 bits et 64 bits d’Office
ms.date: 07/04/2021
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Découvrez en quoi la version 32 bits d’Office est compatible avec la version 64 bits d’Office.
localization_priority: Priority
ms.openlocfilehash: e1beaf4217091c1218653df33bd7d99883fb0862
ms.sourcegitcommit: 8dcb4dc4aa066e3d79bcccd9a9aa6cd3f192b3e1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2021
ms.locfileid: "53535891"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a>Compatibilité entre les versions 32 bits et 64 bits d’Office

Découvrez en quoi la version 32 bits d’Office est compatible avec la version 64 bits d’Office.
  
Les applications Office sont disponibles en versions 32 bits et 64 bits. 
  
Les versions 64 bits d’Office vous permettent de déplacer davantage de données pour une fonctionnalité accrue, par exemple lorsque vous travaillez avec de grands nombres dans Microsoft Excel 2010. Lorsque vous écrivez du code 32 bits, vous pouvez utiliser la version 64 bits d’Office sans aucune modification. Toutefois, lorsque vous écrivez du code 64 bits, vous devez vous assurer que votre code contient des mots clés spécifiques et des constantes de compilation conditionnelle pour vous assurer que le code est à compatibilité descendante avec une version antérieure d’Office et que le code approprié est exécuté si vous mélangez du code 32 bits et 64 bits.
  
L’implémentation Visual Basic pour Applications 7.0 (VBA 7) est publiée dans les versions 64 bits d’Office, mais elle fonctionne avec les applications 32 bits et 64 bits. Les modifications décrites dans cet article s’appliquent uniquement aux versions 64 bits d’Office. Utiliser les versions 32 bits de Microsoft Office vous permet d’exploiter les solutions intégrées dans les versions précédentes d’Office sans apporter d’autres modifications.
  
> [!NOTE]
> Par défaut, lorsque vous installez une version 64 bits d’Office, vous installez également la version 32 bits, ainsi que le système 64 bits. Vous devez explicitement sélectionner l’option d’installation de la version 64 bits de Microsoft Office. 
  
Dans VBA 7, vous devez mettre à jour les instructions API Windows existantes (instructions **Declare**) pour qu’elles fonctionnent avec la version 64 bits. De plus, vous devez mettre à jour les pointeurs d’adresse et afficher les handles de fenêtre dans les types définis par l’utilisateur utilisés par ces instructions. Ces questions sont abordées plus en détail dans cet article, ainsi que les problèmes de compatibilité entre les versions 32 bits et 64 bits et les solutions suggérées. 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a>Comparer des systèmes 32 bits et 64 bits
<a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a>

Les applications créées avec les versions 64 bits d’Office peuvent faire référence à de plus grands espaces d’adressage que ceux des versions 32 bits. Cela signifie que vous pouvez utiliser davantage de mémoire physique pour les données qu’auparavant, permettant éventuellement de réduire la charge liée aux transferts incessants de données sur une mémoire physique.
  
En plus de faire référence à des emplacements spécifiques (appelés pointeurs) dans la mémoire physique, vous pouvez également utiliser des adresses pour référencer des identificateurs de fenêtre d’affichage (appelés handles). La taille (en octets) du pointeur ou du handle varie selon que vous utilisez un système 32 bits ou 64 bits. 
  
Si vous voulez exécuter vos solutions existantes avec les versions 64 bits d’Office, tenez compte des points suivants :
  
- Les processus 64 bits natifs dans Office ne peuvent pas charger de fichiers binaires 32 bits. Il s’agit normalement d’un problème courant lorsque vous avez des contrôles Microsoft ActiveX existants et des compléments existants.
    
- Auparavant, VBA ne disposait pas de type de données de pointeur. Vous deviez utiliser des variables 32 bits pour stocker les pointeurs et les handles. Ces variables tronquent désormais les valeurs 64 bits renvoyées par les appels d’API lors de l’utilisation des instructions **Declare**. 
    
## <a name="vba-7-code-base"></a>Base de code VBA 7
<a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a>

VBA 7 remplace la base de code VBA Office 2007 et versions antérieures. Cette implémentation est disponible dans les versions 32 bits et 64 bits d’Office. Elle fournit deux constantes de compilation conditionnelle : 
  
- **VBA7** : permet de garantir la compatibilité descendante de votre code en testant si votre application utilise VBA 7 ou la version antérieure de VBA. 
    
- **Win64** : teste si le code est en cours d’exécution au format 32 bits ou 64 bits. 
    
À quelques exceptions près, les macros d’un document qui fonctionnent dans la version 32 bits de l’application fonctionnent également dans la version 64 bits.
  
## <a name="activex-control-and-com-add-in-compatibility"></a>Compatibilité des contrôles ActiveX et des compléments COM
<a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a>

Les contrôles ActiveX 32 bits existants ne sont pas compatibles avec les versions 64 bits d’Office. Pour les contrôles ActiveX et les objets COM :
  
- Si vous disposez du code source, vous pouvez générer une version 64 bits vous-même.
- Si vous n’avez pas le code source, contactez le fournisseur pour obtenir une version mise à jour.
    
Les processus 64 bits natifs d’Office ne peuvent pas charger les fichiers binaires 32 bits. Cela inclut les contrôles communs de **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) et les contrôles de **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar). Ces contrôles ont été installés par les versions 32 bits d’Office antérieures à Office 2010. Lorsque vous migrez le code vers les versions 64 bits d’Office, vous devez trouver une alternative pour vos solutions VBA existantes qui utilisent ces contrôles. 
  
## <a name="api-compatibility"></a>Compatibilité de l’API
<a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a>

L’association de VBA et de bibliothèques de types vous offre de nombreuses fonctionnalités utiles pour créer des applications Office. Cependant, vous devez parfois communiquer directement avec le système d’exploitation et d’autres composants de l’ordinateur, par exemple lorsque vous gérez la mémoire ou des processus, lorsque vous travaillez avec des éléments d’interface utilisateur comme des fenêtres et des contrôles ou lorsque vous modifiez le Registre Windows. Dans ces scénarios, votre meilleure option consiste à utiliser l’une des fonctions externes incorporées dans les fichiers DLL. Vous pouvez le faire dans VBA en passant des appels d’API à l’aide des instructions **Declare**. 
  
> [!NOTE]
> Microsoft fournit le fichier Win32API.txt qui contient 1 500 instructions Declare et un outil permettant de copier l’instruction **Declare** que vous souhaitez dans votre code. Cependant, ces instructions s’appliquent aux systèmes 32 bits et doivent être converties en 64 bits à l’aide des informations indiquées plus loin dans cet article. Les instructions **Declare** existantes ne seront pas compilées dans VBA 64 bits avant d’avoir été indiquées comme fiables pour 64 bits à l’aide de l’attribut **PtrSafe**. Vous trouverez des exemples de ce type de conversion sur le site web de Jan Karel Pieterse, Excel MVP à l’adresse suivante [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp). Le [guide d’utilisateur de l’inspecteur de compatibilité du code Office](https://docs.microsoft.com/previous-versions/office/office-2010/ee833946(v=office.14)) est un outil particulièrement utile pour examiner la syntaxe des instructions API **Declare** pour l’attribut **PtrSafe**, le cas échéant, et le type de renvoi approprié. 
  
Les instructions **Declare** ressemblent à ce qui suit, selon que vous appelez une sous-routine (qui n’a aucune valeur de retour) ou une fonction (qui a une valeur de retour). 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

La fonction **SubName** ou **FunctionName** est remplacée par le vrai nom de la procédure décrite dans le fichier DLL et correspond au nom utilisé lorsque la procédure est appelée à partir du code VBA. Vous pouvez également spécifier un argument **AliasName** pour le nom de la procédure. Le nom du fichier DLL qui contient la procédure appelée suit le mot-clé **Lib**. Enfin, la liste d’arguments contient les paramètres et les types de données qui doivent être transmis à la procédure. 
  
L’instruction **Declare** suivante ouvre une *subkey* dans le Registre Windows et remplace sa valeur. 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

L’entrée Windows.h (handle de fenêtre) pour la fonction **RegOpenKeyA** est comme suit : 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

Dans Visual C et Microsoft Visual C++, l’exemple précédent se compile correctement pour les versions 32 bits et 64 bits. Cela est dû au fait que HKEY est défini comme un pointeur, dont la taille reflète la taille de mémoire de la plateforme dans laquelle le code est compilé.
  
Dans les versions précédentes de VBA, il n’existait aucun type de données de pointeur spécifique ; le type de données **Long** était par conséquent toujours utilisé. Le type de données **Long** étant toujours 32 bits, cela provoque un échec en cas d’utilisation sur un système doté d’une mémoire 64 bits car les 32 bits supérieurs peuvent être tronqués ou peuvent remplacer d’autres adresses mémoire. L’une ou l’autre de ces situations peut provoquer un comportement inattendu ou un blocage système. 
  
Pour résoudre ce problème, VBA inclut un véritable type de données *pointeur* : **LongPtr**. Ce nouveau type de données vous permet d’écrire correctement l’instruction **Declare** d’origine comme suit : 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

Ce type de données et le nouvel attribut **PtrSafe** vous permettent d’utiliser cette instruction **Declare** sur les systèmes 32 bits ou 64 bits. L’attribut **PtrSafe** indique au compilateur VBA que l’instruction **Declare** concerne la version 64 bits d’Office. Sans cet attribut, l’utilisation de l’instruction **Declare** dans un système 64 bits entraîne une erreur de compilation. L’attribut **PtrSafe** est facultatif sur la version 32 bits d’Office. Cela permet aux instructions **Declare** existantes de fonctionner comme elles l’ont toujours fait. 
  
Le tableau suivant fournit des informations supplémentaires sur le nouveau qualificateur et les nouveaux types de données, ainsi qu’un autre type de données, deux opérateurs de conversion et trois fonctions.
  
|Type|Item|Description|
|:-----|:-----|:-----|
|Qualificateur  <br/> |**PtrSafe** <br/> |Indique que l’instruction **Declare** est compatible avec 64 bits. Cet attribut est obligatoire sur les systèmes 64 bits.<br/> |
|Type de données  <br/> |**LongPtr** <br/> |Type de données variable qui est un type de données de 4 octets sur les versions 32 bits et un type de données de 8 octets sur les versions 64 bits de Microsoft Office. Il s’agit de la méthode recommandée pour déclarer un pointeur ou un handle pour le nouveau code, mais également pour le code hérité s’il doit s’exécuter dans la version 64 bits d’Office. Il est uniquement pris en charge dans le runtime VBA 7 sur 32 bits et 64 bits. Notez que vous pouvez lui attribuer des valeurs numériques, mais pas des types numériques.  <br/> |
|Type de données  <br/> |**LongLong** <br/> |Il s’agit d’un type de données de 8 octets qui est disponible uniquement dans les versions 64 bits de Microsoft Office. Vous pouvez affecter des valeurs numériques, mais pas des types numériques (pour éviter la troncation).  <br/> |
|Opérateur de conversion  <br/> |**CLngPtr** <br/> |Convertit une expression simple en un type de données **LongPtr**.  <br/> |
|Opérateur de conversion  <br/> |**CLngLng** <br/> |Convertit une expression simple en un type de données **LongLong**.  <br/> |
|Fonction  <br/> |**VarPtr** <br/> |Convertisseur de variante. Renvoie un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).<br/> |
|Fonction  <br/> |**ObjPtr** <br/> |Convertisseur d’objet. Renvoie un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).<br/> |
|Fonction  <br/> |**StrPtr** <br/> |Convertisseur de chaîne. Renvoie un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).<br/> |
   
L’exemple suivant montre comment utiliser certains de ces éléments dans une instruction **Declare**. 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

Notez que les instructions **Declare** sans attribut **PtrSafe** sont considérées comme non compatibles avec la version 64 bits d’Office. 
  
Il existe deux constantes de compilation conditionnelle : **VBA7** et **Win64**. Pour assurer la compatibilité descendante avec les versions antérieures de Microsoft Office, utilisez la constante **VBA7** (c’est le cas le plus typique) pour empêcher d’utiliser le code 64 bits dans la version antérieure d’Office. Pour le code qui est différent entre la version 32 bits et la version 64 bits, comme l’appel d’une API de mathématiques qui utilise **LongLong** pour sa version 64 bits et **Long** pour sa version 32 bits, utilisez la constante **Win64**. Le code suivant montre l’utilisation de ces deux constantes. 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

Pour résumer, si vous écrivez du code 64 bits et que vous comptez l’utiliser dans les versions précédentes d’Office, utilisez la constante de compilation conditionnelle **VBA7**. Cependant, si vous écrivez du code 32 bits dans Office, ce code fonctionne tel quel dans les versions précédentes d’Office sans passer par la constante de compilation. Si vous voulez vérifier que vous utilisez les instructions 32 bits pour les versions 32 bits et les instructions 64 bits pour les versions 64 bits, votre meilleure option consiste à utiliser la constante de compilation conditionnelle **Win64**. 
  
## <a name="using-conditional-compilation-attributes"></a>Utilisation des attributs de compilation conditionnelle
<a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a>

L’exemple suivant montre le code VBA destiné aux versions 32 bits qui doit être mis à jour. Notez que les types de données du code hérité sont mis à jour pour utiliser **LongPtr**, car ils font référence aux handles ou aux pointeurs. 
  
### <a name="vba-code-written-for-32-bit-versions"></a>Code VBA destiné aux versions 32 bits
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As LongPtr
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a>Code VBA réécrit pour les versions 64 bits
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a>

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a>Quand dois-je utiliser la version 64 bits d’Office ?
  
La question est plutôt de savoir quelle application hôte (Excel, Word, etc.) vous utilisez. Par exemple, Excel est en mesure de gérer des feuilles de calcul beaucoup plus grandes avec la version 64 bits de Microsoft Office.
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a>Puis-je installer des versions 64 bits et 32 bits d’Office côte à côte ?
  
Non.
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a>Quand dois-je convertir des paramètres Long en LongPtr ?
  
Vous devez vérifier la documentation de l’API Windows sur le Microsoft Developers Network pour la fonction que vous voulez appeler. Les handles et les pointeurs doivent être convertis en **LongPtr**. Par exemple, la documentation relative à [RegOpenKeyA](/windows/win32/api/winreg/nf-winreg-regopenkeyexa.md) fournit la signature suivante : 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

Les paramètres sont définis comme suit :
  
|Parameter|Description|
|:-----|:-----|
|hKey [dans]  <br/> |Une *handle* vers une clé de Registre ouverte.  <br/> |
|lpSubKey [dans, facultatif]  <br/> |Le nom de la sous-clé de Registre à ouvrir.  <br/> |
|ulOptions  <br/> |Ce paramètre est réservé et doit être égal à zéro.  <br/> |
|samDesired [dans]  <br/> |Masque qui spécifie les droits d’accès souhaités à la clé.  <br/> |
|phkResult [out]  <br/> |Un *pointeur* vers une variable qui reçoit une handle vers la clé ouverte.  <br/> |
   
Dans [Win32API_PtrSafe.txt](/office/troubleshoot/office/win32api_ptrsafe-with-64-bit-support.md), l’instruction **Declare** se définit comme suit : 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a>Dois-je convertir les pointeurs et les handles dans les structures ?
  
Oui. Observez le type **MSG** dans Win32API_PtrSafe.txt : 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a>Quand dois-je utiliser strptr, varpt et objptr ?
  
Vous devez utiliser ces fonctions pour récupérer respectivement des pointeurs vers des chaînes, des variables et des objets. Sur la version 64 bits d’Office, ces fonctions renvoient un **LongPtr** de 64 bits, qui peut être transféré à l’instruction **Declare**. L’utilisation de ces fonctions n’a pas changé des versions précédentes de VBA. La seule différence est qu’elles renvoient désormais un **LongPtr**.
  
## <a name="see-also"></a>Voir aussi
<a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a>

- [Anatomie d’une instruction Declare](https://docs.microsoft.com/previous-versions/aa671659(v=vs.71))
