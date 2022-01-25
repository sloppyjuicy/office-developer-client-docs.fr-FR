---
title: Création de fichiers XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- dll [excel 2007], appel dans excel, fonction xlAutoFree [Excel 2007], fonction xlAutoFree12 [Excel 2007], xlcall32.lib [Excel 2007], fonction xlAutoRegister [Excel 2007], xlcall.cpp [Excel 2007], fonction xlAutoRemove [Excel 2007], fonction xlAddInManagerInfo [Excel 2007], fonction xlAutoAdd [Excel 2007], fonction xlAutoOpen [Excel 2007], fonction xlAutoClose [Excel 2007], DLL [Excel 2007], transformation en XLL, XLL [Excel 2007] appel dans Excel, fonction xlAutoRegister12 [Excel 2007], xlcall.h [Excel 2007], fonction xlAddInManagerInfo12 [Excel 2007]
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
ms.localizationpriority: high
ms.openlocfilehash: 7a2ae2d4a24142efc4300833283abdbc1644f99c
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199009"
---
# <a name="creating-xlls"></a>Création de fichiers XLL

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Si votre DLL est autonome ou repose uniquement sur d’autres bibliothèques, vous devez savoir comment activer Microsoft Excel pour accéder à ses fonctions et commandes. Pour plus d’informations, reportez-vous à la rubrique [Accès aux DLL dans Excel](how-to-access-dlls-in-excel.md). 
  
Toutefois, si votre DLL a besoin d’accéder aux fonctionnalités d’Excel (par exemple, pour obtenir le contenu d’une cellule, pour appeler une fonction de feuille de calcul ou pour interroger Excel en vue d’obtenir des informations sur l’espace de travail), votre code doit être en mesure de rappeler Excel.
  
L’API Excel C offre plusieurs fonctions qui permettent aux DLL de rappeler Excel. Pour y accéder, le DLL doit être lié statiquement au moment de la compilation avec la bibliothèque Excel 32 bits xlcall32.lib. La bibliothèque statique est téléchargeable auprès de Microsoft dans le cadre du SDK XLL Microsoft Excel 2013, qui inclut les versions 32 et 64 bits de cette bibliothèque.
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Activation du rappel dans Excel pour les DLL

Pour qu’une DLL puisse accéder aux fonctionnalités d’Excel et obtenir ou définir des informations sur l’espace de travail, elle doit tout d’abord obtenir les adresses des fonctions de rappel Excel **Excel4**, **Excel4v**, **Excel 12** et **Excel12v**. Les deux dernières ont été introduites dans Excel 2007 et sont disponibles dans les versions suivantes. Pour accéder à toutes ces fonctions, le projet de DLL doit contenir des références aux fichiers suivants du SDK XLL Excel 2013. Si vous voulez uniquement accéder aux deux premiers rappels (dans n’importe quelle version d’Excel), votre projet doit seulement inclure les deux premiers fichiers.
  
### <a name="xlcallh"></a>Xlcall.h

Le fichier Xlcall.h contient les éléments suivants :
  
- Prototypes de fonction pour toutes les fonctions de rappel.
    
- Définitions des structures de données que les rappels utilisent pour échanger des données entre le DLL/XLL et Excel, et définitions des constantes de type de données.
    
- Définitions de la fonction d’API C et des équivalents de commande de la feuille de calcul, fonctions macro de la feuille et commandes Excel prises en charge.
    
- Définitions des valeurs de retour de la fonction de rappel.
    
Vous devez utiliser la directive **#include** pour ce fichier, directement ou indirectement à partir d’un autre fichier d’en-tête, dans tous les fichiers qui accèdent à l’API C ou qui gèrent les types de données que l’API C utilise. 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

La bibliothèque Xlcall32.lib exporte les deux premiers rappels, **Excel4** et **Excel4v**, ainsi que la fonction **XlCallVer**. Sans une référence à cette bibliothèque dans votre projet, l’éditeur de liens ne peut pas créer le XLL si vous avez utilisé l’un de ces rappels dans votre code. (Vous pouvez obtenir les adresses de ces fonctions en créant un lien dynamique vers le fichier équivalent Xlcall32.dll copié sur votre système dans le cadre d’une installation Excel standard.) 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

Les rappels Excel **Excel 12** et **Excel12v** ne sont pas exportés dans Xlcall32.lib. Cela garantit que les projets XLL que vous créez à partir d’Excel 2007 fonctionnent également avec les versions antérieures d’Excel. Le module Xlcall.cpp contient le code des fonctions **Excel12** et **Excel12v**, qui appellent un point d’entrée Excel dans les versions à partir d’Excel 2007 ou renvoient une valeur safe-error si vous exécutez une version antérieure d’Excel. Vous devez inclure ce module dans votre projet si vous voulez créer un XLL qui s’exécute à partir de la version 2007 d’Excel, et qui soit capable d’utiliser les nouveaux types de données qui traitent les grilles plus grandes et des chaînes Unicode plus longues. 
  
> [!NOTE]
> Depuis le SDK Excel 2010, ce fichier peut être compilé pour des XLL 32 et 64 bits. 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>Transformation de DLL et XLL : fonctions d’interface du gestionnaire de compléments

Un fichier XLL est une DLL qui exporte plusieurs procédures appelées par Excel ou par le gestionnaire de compléments Excel. Ces procédures sont décrites brièvement dans le présent document et présentées en détail dans [Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md). Tous ces rappels de DLL commencent par le préfixe **xlAuto**. Seul l’un d’entre eux est obligatoire, à savoir la commande **xlAutoOpen**. Celle-ci est appelée lors de l’activation du complément, et est généralement utilisée pour inscrire les fonctions et commandes du XLL dans Excel, ainsi que pour effectuer d’autres tâches d’initialisation. Les signatures de fonction ainsi que des exemples d’implémentations de toutes les fonctions **xlAuto** sont fournis dans les sections suivantes. 
  
Même si **xlAutoOpen** est le seul de ces rappels à être obligatoire, votre complément peut également avoir besoin d’en exporter d’autres, en fonction de son comportement. 
  
Excel 2007 a introduit un nouveau type de données, **XLOPER12**, pour s’adapter aux grilles plus grandes et prendre en charge les chaînes Unicode longues. **XLOPER12** est décrit plus loin dans cette rubrique. Tandis que les fonctions **xlAuto** prennent ou renvoient l’ancien type de données **XLOPER**, de nouvelles versions de ces fonctions qui utilisent les types de données **XLOPER12** ont été introduites Excel 2007. À l’exception de **xlAutoFree12**, que vous devez parfois implémenter pour éviter les fuites de mémoire de **XLOPER12**, vous pouvez ignorer en toute sécurité les fonctions **xlAuto** de la version 12. Le cas échéant, à partir d’Excel 2007, Excel appelle les versions **XLOPER**. 
  
### <a name="xlautoopen"></a>xlAutoOpen

Excel appelle la fonction [xlAutoOpen](xlautoopen.md) à chaque fois que la XLL est activée. Le complément est activé au début d’une session Excel s’il a été actif dans la dernière session Excel qui a pris fin normalement. Le complément est activé s’il est chargé au cours d’une session d’Excel. Le complément peut être désactivé et réactivé pendant une session Excel et la fonction est appelée lors de la réactivation. 
  
Vous devez utiliser **xlAutoOpen** pour inscrire les fonctions et commandes XLL, initialiser les structures de données, personnaliser l’interface utilisateur et ainsi de suite. 
  
Si votre complément implémente et exporte la fonction [xlAutoRegister](xlautoregister-xlautoregister12.md) ou la fonction [xlAutoRegister12](xlautoregister-xlautoregister12.md), Excel peut tenter d’activer et d’inscrire une fonction ou une commande sans appeler préalablement la fonction **xlAutoOpen**. Dans ce cas, assurez-vous que votre complément est suffisamment initialisé pour que votre fonction ou commande fonctionne correctement. Si ce n’est pas le cas, faites échouer la tentative d’inscription de la fonction ou de la commande, ou procédez à l’initialisation nécessaire. 
  
### <a name="xlautoclose"></a>xlAutoClose

Excel appelle la fonction [xlAutoClose](xlautoclose.md) à chaque fois que la XLL est désactivée. Le complément est désactivé lorsqu’une session Excel se termine normalement. Si l’utilisateur désactive le complément au cours d’une session Excel, la fonction est appelée. 
  
Vous devez utiliser **xlAutoClose** pour annuler l’inscription des fonctions et commandes, libérer des ressources, annuler les personnalisations, etc. 
  
> [!NOTE]
> Un problème connu survient lors de l’annulation d’inscription des fonctions et commandes. Pour plus d’informations, reportez-vous à la rubrique [Problèmes connus concernant le développement de XLL Excel](known-issues-in-excel-xll-development.md). 
  
### <a name="xlautoadd"></a>xlAutoAdd

Excel appelle la fonction [xlAutoAdd](xlautoadd.md) chaque fois que l’utilisateur active le XLL pendant une session Excel à l’aide du Gestionnaire de compléments. Cette fonction n’est pas appelée lorsqu’Excel démarre et charge un complément préinstallé. 
  
Vous pouvez utiliser cette fonction pour afficher une boîte de dialogue personnalisée qui indique à l’utilisateur que le complément a été activé, qu’il peut lire ou écrire dans le registre ou vérifier les informations sur les licences.
  
### <a name="xlautoremove"></a>xlAutoRemove

Excel appelle la fonction [xlAutoRemove](xlautoremove.md) à chaque fois que l’utilisateur désactive le XLL au cours d’une session Excel à l’aide du Gestionnaire de compléments. Cette fonction n’est pas appelée lors de la fermeture normale ou anormale d’une session Excel lorsque le complément est installé. 
  
Vous pouvez utiliser cette fonction pour afficher une boîte de dialogue personnalisée qui indique à l’utilisateur que le complément a été désactivé, ou qu’il peut lire ou écrire dans le registre.
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

Excel appelle la fonction [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) lorsque le Gestionnaire de compléments est appelé pour la première fois dans une session Excel. Si Excel transmet un argument égal à 1, cette fonction doit renvoyer une chaîne (en règle générale, le nom du complément) ; sinon, elle doit renvoyer **#VALUE!**.
  
À partir d’Excel 2007, Excel appelle de préférence la fonction **xlAddInManagerInfo12** plutôt que **xlAddInManagerInfo** si elle est exportée par le XLL. La fonction **xlAddInManagerInfo12** doit fonctionner de la même manière que **xlAddInManagerInfo** afin d’éviter les différences propres à chaque version dans le comportement du fichier XLL. La fonction **xlAddInManagerInfo12** doit renvoyer un type de données **XLOPER12**, alors que **xlAddInManagerInfo** doit renvoyer le type **XLOPER**. 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

Excel appelle la fonction [xlAutoRegister](xlautoregister-xlautoregister12.md) chaque fois qu’un appel à la fonction XLM **REGISTER** ou à la fonction API C équivalente [xlfRegister](xlfregister-form-1.md) a été effectué, avec les types de retour et d’argument manquants pour la fonction qui fait l’objet de l’inscription. La fonction **xlAutoRegister** permet au XLL de rechercher ses listes internes de fonctions et de commandes exportées pour inscrire la fonction avec l’argument et renvoyer les types spécifiés. 
  
À partir d’Excel 2007, Excel appelle la fonction **xlAddInRegister12** plutôt que la fonction **xlAddInRegister** si elle est exportée par le XLL. 
  
> [!NOTE]
> Si **xlAddInRegister**/ **xlAddInRegister12** tente d’inscrire la fonction sans fournir les types d’argument et de retour, une boucle d’appel récursive survient et finit par faire déborder la pile d’appel et par entraîner la fermeture ou le blocage d’Excel. 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

Excel appelle la fonction [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) immédiatement après qu’une fonction de feuille de calcul XLL a renvoyé un type de données **XLOPER**/ **XLOPER12** avec un indicateur qui signale à Excel que le XLL a toujours de la mémoire à libérer. Le XLL peut ainsi renvoyer des matrices, des chaînes et des références externes allouées dynamiquement vers la feuille de calcul sans pertes de mémoire. À partir d’Excel 2007, le type de données **XLOPER12** est pris en charge. Pour plus d’informations, reportez-vous à la rubrique [Gestion de la mémoire dans Excel](memory-management-in-excel.md).
  
> [!NOTE]
> À partir d’Excel 2007, si Excel est configuré pour utiliser le recalcul multithread de feuille de calcul, la fonction **xlAutoFree**/ **xlAutoFree12** est appelée sur le thread qui vient d’être utilisé pour appeler la fonction qui l’a renvoyée. L’appel à **xlAutoFree**/ **xlAutoFree12** est toujours effectué avant que d’autres cellules de la feuille de calcul soient évaluées sur ce thread. Cela simplifie la conception thread-safe dans votre XLL. Pour plus d’informations, reportez-vous à la rubrique [Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md). 
  
### <a name="creating-64-bit-xlls"></a>Création de XLL 64 bits

Excel et les fonctions définies par l’utilisateur peuvent s’exécuter sur des systèmes d’exploitation 64 bits pour bénéficier de meilleures performances que sur des systèmes d’exploitation 32 bits. Excel transmet les valeurs dans des structures **XLOPER12** qui contiennent des informations sur les types de données. Soyez prudent lorsque vous effectuez des conversions entre les valeurs de la structure **XLOPER12** et des types natifs tels que **int** ou des pointeurs, afin de conserver les valeurs dans le type le plus étendu. 
  
## <a name="see-also"></a>Voir aussi



[Appel des fonctions XLL à partir de l’Assistant Fonction ou des boîtes de dialogue Remplacer](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)
  
[Développement de XLL de Excel](developing-excel-xlls.md)

