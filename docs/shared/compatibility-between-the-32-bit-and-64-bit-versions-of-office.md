---
title: Compatibilité entre les versions 32 bits et 64 bits d’Office
ms.date: 04/27/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Découvrez comment la version 32 bits d’Office est compatible avec la version 64 bits d’Office.
ms.openlocfilehash: eeff11f11d4f2595b7111c0233703d09b1c46651
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390939"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a>Compatibilité entre les versions 32 bits et 64 bits d’Office

Découvrez comment la version 32 bits d’Office est compatible avec la version 64 bits d’Office.
  
Applications Office sont disponibles en versions 32 bits et 64 bits. 
  
Les versions 64 bits d’Office permettent de déplacer des données pour des capacités, par exemple, lorsque vous travaillez avec un grand nombre de Microsoft Excel 2010. Lorsque vous écrivez du code 32 bits, vous pouvez utiliser la version 64 bits d’Office sans aucune modification. Toutefois, lorsque vous écrivez du code 64 bits, vous devez vous assurer que votre code contienne des constantes de compilation conditionnelle pour vous assurer que le code est compatible avec la version antérieure d’Office et les mots clés spécifiques, et que le code est en cours d’exécution si vous combinaison de code 32 bits et 64 bits.
  
Visual Basic pour Applications 7.0 (7 VBA) est publié dans les versions 64 bits d’Office, et elle fonctionne avec les applications 32 bits et 64 bits. Les modifications décrites dans cet article s’appliquent uniquement aux versions 64 bits d’Office. Utilisant les versions 32 bits d’activation de Microsoft Office vous permet d’utiliser les solutions créées dans les versions précédentes d’Office sans aucune modification.
  
> [!NOTE]
> Par défaut, lorsque vous installez une version 64 bits d’Office, vous installez également la version 32 bits est installé avec le système 64 bits. Vous devez sélectionner explicitement l’option d’installation de Microsoft Office 64 bits version. 
  
Dans VBA 7, vous devez mettre à jour des instructions d’API Windows existantes (les instructions**Declare** ) pour fonctionner avec la version 64 bits. En outre, vous devez mettre à jour des pointeurs d’adresse et afficher les poignées de fenêtre dans les types définis par l’utilisateur qui sont utilisés par ces instructions. Cette opération est abordée plus en détail dans cet article, ainsi que les problèmes de compatibilité entre les versions 32 bits et 64 bits et les solutions suggérées. 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a>Comparaison des systèmes 32 bits et 64 bits
<a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a>

Les applications créées avec les versions 64 bits d’Office peuvent référencer des espaces d’adressage plus grandes que les versions 32 bits. Cela signifie que vous pouvez utiliser davantage de mémoire physique pour que les données avant, ce qui peut réduire la surcharge passé le transfert de données dans la mémoire physique
  
En plus de faire référence à des emplacements spécifiques (appelés pointeurs) dans la mémoire physique, vous pouvez également utiliser des adresses pour référencer des identificateurs de fenêtre d’affichage (appelés poignées). La taille (en octets) du pointeur ou handle varie selon que vous utilisez un système 32 bits ou 64 bits. 
  
Si vous souhaitez exécuter vos solutions existantes avec les versions 64 bits d’Office, prenez en compte les éléments suivants :
  
- Impossible de charger le processus 64 bits natifs dans Office binaires 32 bits. Ce programme devrait être des problèmes lorsque vous avez des contrôles Microsoft ActiveX existants et compléments existants.
    
- VBA n’a pas été précédemment ont un type de données pointeur, afin que vous deviez utiliser des variables 32 bits pour stocker des pointeurs et les poignées. Ces variables tronquent 64 bits les valeurs renvoyées par les appels d’API lors de l’utilisation des instructions **Declare** . 
    
## <a name="vba-7-code-base"></a>Base de code VBA 7
<a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a>

VBA 7 remplace le code VBA dans Office 2007 et versions antérieures. VBA 7 est disponible dans les versions 32 bits et 64 bits d’Office. Il fournit des deux constantes de compilation conditionnelle : 
  
- **VBA7** - permet d’assurer la compatibilité descendante de votre code en vérifiant si votre application est à l’aide de VBA 7 ou la version précédente de VBA. 
    
- **Win64** Teste l’exécution du code 32 bits ou 64 bits. 
    
À quelques exceptions près, les macros dans un document qui fonctionnent dans la version 32 bits de l’application fonctionnent également dans la version 64 bits.
  
## <a name="activex-control-and-com-add-in-compatibility"></a>Contrôle ActiveX et la compatibilité des compléments COM
<a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a>

Existants les contrôles ActiveX 32 bits, ne sont pas compatibles avec les versions 64 bits d’Office. Pour les contrôles ActiveX et les objets COM :
  
- Si vous avez le code source, générer une version 64 bits vous-même.
- Si vous ne disposez pas du code source, contactez le fournisseur pour obtenir une version mise à jour.
    
Impossible de charger le processus 64 bits natifs dans Office binaires 32 bits. Cela inclut les contrôles courants de **MSComCtl** (TabStrip, barre d’outils, StatusBar, ProgressBar, TreeView, ListViews, ImageList, curseur, ImageComboBox) et les contrôles de **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar). Ces contrôles ont été installés par les versions 32 bits d’Office antérieure à Office 2010. Vous devez trouver une alternative de vos solutions VBA existantes qui utilisent ces contrôles lorsque vous migrez le code pour les versions 64 bits d’Office. 
  
## <a name="api-compatibility"></a>Compatibilité des API
<a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a>

La combinaison de bibliothèques VBA et de type vous offre de nombreuses fonctionnalités pour créer des applications Office. Toutefois, vous devez parfois communiquent directement avec le système d’exploitation et d’autres composants, tels que lorsque vous gérez mémoire ou les processus, lorsque vous travaillez avec des contrôles et des fenêtres de linke des éléments de l’interface utilisateur, ou lorsque vous modifiez le Registre Windows. Dans ces scénarios, la meilleure solution consiste à utiliser l’une des fonctions externes incorporés dans des fichiers DLL. Cela dans VBA en effectuant des appels d’API à l’aide des instructions **Declare** . 
  
> [!NOTE]
> Microsoft propose un fichier Win32API.txt qui contient les instructions Declare 1500 et un outil pour copier l’instruction **Declare** que vous souhaitez dans votre code. Toutefois, ces instructions sont pour les systèmes 32 bits et doit être converties en 64 bits en utilisant les informations décrites plus loin dans cet article. Les instructions **Declare** existantes ne seront pas compilées dans VBA 64 bits jusqu'à ce qu’ils ont été marquées comme sûrs pour 64 bits à l’aide de l’attribut **PtrSafe** . Vous trouverez des exemples de ce type de conversion sur le site Web de Pieterse Excel MVP Jan Karel à [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp). Le [guide de l’utilisateur Office Code Compatibility Inspector](https://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) est un outil utile pour inspecter la syntaxe des instructions d’API **Declare** pour l’attribut **PtrSafe** , le cas échéant, et le type de retour. 
  
Les instructions **Declare** ressembler à un des éléments suivants, selon que vous l’appelez une sous-routine (qui ne renvoie aucune valeur) ou une fonction (qui a une valeur de retour). 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

La fonction **nomsub** ou **suivantes** est remplacée par le nom réel de la procédure dans le fichier DLL et représente le nom qui est utilisé lorsque la procédure est appelée à partir du code VBA. Vous pouvez également spécifier un argument **AliasName** pour le nom de la procédure. Le nom du fichier DLL qui contient la procédure appelée suit le mot clé **Lib** . Et enfin, la liste d’arguments contient les paramètres et les types de données qui doivent être transmis à la procédure. 
  
L’instruction **Declare** suivante ouvre une *sous-clé* dans le Registre Windows et remplace sa valeur. 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

L’entrée Windows.h (handle de fenêtre) pour la fonction **RegOpenKeyA** est la suivante : 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

Dans Visual C# et Microsoft Visual C++, l’exemple précédent se compile correctement pour 32 bits et 64 bits. Il s’agit comme HKEY est définie comme un pointeur dont la taille reflète la taille de la mémoire de la plateforme de compilation dans le code.
  
Dans les versions précédentes de VBA, il a été aucun type de données pointeur spécifique afin que le type de données **Long** a été utilisé. Et parce que le type de données **Long** est toujours 32 bits, cette sauts lorsqu’elle est utilisée sur un système 64 bits, car les supérieures 32 bits risquent d’être tronqués ou peuvent remplacer les autres adresses de mémoire. Une de ces situations peut entraîner des incidents système ou de comportement imprévisibles. 
  
Pour résoudre ce problème, VBA inclut un type de données de la valeur true *pointeur* : **LongPtr**. Ce nouveau type de données vous permet d’écrire l’instruction **Declare** d’origine correctement en tant que : 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

Ce type de données et le nouvel attribut **PtrSafe** permettent d’utiliser cette instruction **Declare** sur les systèmes 32 bits ou 64 bits. L’attribut **PtrSafe** indique au compilateur VBA que l’instruction **Declare** est ciblée pour la version 64 bits d’Office. Sans cet attribut, à l’aide de l’instruction **Declare** dans un système 64 bits provoquera une erreur de compilation. L’attribut **PtrSafe** est facultatif pour la version 32 bits d’Office. Ainsi, les instructions **Declare** existantes à fonctionner comme ils ont toujours. 
  
Le tableau suivant fournit plus d’informations sur le nouveau qualificateur et typeas de données ainsi que d’un autre type de données, deux opérateurs de conversion et trois fonctions.
  
|Type|Élément|Description|
|:-----|:-----|:-----|
|Qualificateur  <br/> |**PtrSafe** <br/> |Indique que l’instruction **Declare** est compatible 64 bits. Cet attribut est obligatoire sur les systèmes 64 bits.<br/> |
|Type de données  <br/> |**LongPtr** <br/> |Un type de données de la variable qui est un type de données de 4 octets sur les versions 32 bits et un type de données de 8 octets sur les versions 64 bits de Microsoft Office. Il est recommandé de déclarer un pointeur ou un handle pour le nouveau code mais aussi pour code hérité si elle doit s’exécuter dans la version 64 bits d’Office. Il est uniquement pris en charge dans le runtime VBA 7 sur 32 bits et 64 bits. Notez que vous pouvez affecter des valeurs numériques à il mais types numériques pas.  <br/> |
|Type de données  <br/> |**LongLong** <br/> |Il s’agit d’un type de données de 8 octets qui est disponible uniquement dans les versions 64 bits de Microsoft Office. Vous pouvez affecter des valeurs numériques, mais des types non numériques (pour éviter la troncation).  <br/> |
|Opérateur de conversion  <br/> |**CLngPtr** <br/> |Convertit une expression simple en un type de données **LongPtr**.  <br/> |
|Opérateur de conversion  <br/> |**CLngLng** <br/> |Convertit une expression simple en un type de données **LongLong**.  <br/> |
|Fonction  <br/> |**VarPtr** <br/> |Convertisseur de variant. Retourne un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).<br/> |
|Fonction  <br/> |**ObjPtr** <br/> |Convertisseur d’objet. Retourne un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).<br/> |
|Fonction  <br/> |**StrPtr** <br/> |Convertisseur de chaîne. Retourne un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).<br/> |
   
L’exemple suivant montre comment utiliser certains de ces éléments dans une instruction **Declare**. 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

Notez que les instructions **Declare** sans attribut **PtrSafe** sont considérées comme non compatibles avec la version 64 bits d’Office. 
  
Il existe deux constantes de compilation conditionnelle : **VBA7** et **Win64**. Pour garantir la compatibilité descendante avec les versions précédentes de Microsoft Office, vous utilisez la constante **VBA7** (c’est le cas plus courant) pour empêcher l’utilisation de la version antérieure d’Office 64 bits. Pour le code qui est différente de la version 32 bits et la version 64 bits, telles que l’appel mathématique **Long** et les API qui utilise **LongLong** pour la version 64 bits pour la version 32 bits, vous utilisez la constante **Win64** . Le code suivant illustre l’utilisation de ces deux constantes. 
  
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

Pour résumer, si vous écrivez du code 64 bits et envisagez d’utiliser dans les versions précédentes d’Office, vous devez utiliser la constante de compilation conditionnelle **VBA7** . Toutefois, si vous écrivez du code 32 bits dans Office, que ce code fonctionne comme dans les versions antérieures d’Office sans devoir pour la constante de compilation. Si vous voulez vous assurer que vous utilisez les instructions 32 bits pour les versions 32 bits et 64 bits les instructions pour les versions 64 bits, la meilleure solution consiste à utiliser la constante de compilation conditionnelle **Win64** . 
  
## <a name="using-conditional-compilation-attributes"></a>Utilisation d’attributs de compilation conditionnelle
<a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a>

L’exemple suivant montre le code VBA écrit pour 32 bits qui doit être mis à jour. Notez les types de données dans le code hérité qui sont mis à jour pour utiliser **LongPtr** , car elles référencent handles ou pointeurs. 
  
### <a name="vba-code-written-for-32-bit-versions"></a>Code VBA écrit pour les versions 32 bits
  
```vb
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
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a>Réécrit pour les versions 64 bits du code VBA
  
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

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a>Quand dois-je utiliser la version 64 bits d’Office ?
  
Il s’agit plus une question de l’application hôte (Excel, Word, etc.) que vous utilisez. Par exemple, Excel est en mesure de gérer la plus grande quantité feuilles de calcul avec la version 64 bits de Microsoft Office.
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a>Puis-je installer les versions 32 bits et 64 bits d’Office côte à côte ?
  
Non.
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a>Quand dois-je convertir paramètres longs à LongPtr ?
  
Vous devez consulter la documentation de l’API Windows sur le réseau de développeurs Microsoft pour la fonction à appeler. Les poignées et pointeurs doivent être convertie en **LongPtr**. Par exemple, la documentation pour [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) fournit la signature suivante : 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

Les paramètres sont définis en tant que :
  
|Paramètre|Description|
|:-----|:-----|
|hKey [in]  <br/> |Un *Gérer* une clé de Registre ouverte.  <br/> |
|lpSubKey [in, facultatif]  <br/> |Nom de la sous-clé de Registre à ouvrir.  <br/> |
|ulOptions  <br/> |Ce paramètre est réservé et doit être égal à zéro.  <br/> |
|samDesired [in]  <br/> |Masque qui spécifie les droits d’accès souhaité pour la clé.  <br/> |
|phkResult [out]  <br/> |*Pointeur* vers une variable qui reçoit un handle vers la clé ouvert.  <br/> |
   
Dans [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), l’instruction **Declare** est définie en tant que : 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a>Dois-je convertir des pointeurs et poignées de structures ?
  
Oui. Consultez le type de **message** dans Win32API_PtrSafe.txt : 
  
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

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a>Quand dois-je utiliser strptr et objptr varpt ?
  
Vous devez utiliser ces fonctions pour récupérer des pointeurs vers des chaînes, des variables et des objets, respectivement. Sur la version 64 bits d’Office, ces fonctions renvoient 64-bit **LongPtr**, qui peut être passé aux instructions **Declare** . L’utilisation de ces fonctions n’a pas été modifié à partir de versions antérieures de VBA. La seule différence est qu’elles retournent maintenant **LongPtr**.
  
## <a name="see-also"></a>Voir aussi
<a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a>

- [Anatomie d’une instruction Declare](https://msdn.microsoft.com/library/office/aa671659.aspx)
    

