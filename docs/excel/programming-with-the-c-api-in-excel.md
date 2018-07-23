---
title: Programmation avec l’API C dans Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],programming interfaces [Excel 2007],C API [Excel 2007], when to use,C API [Excel 2007], relation to XLM,Excel programming interfaces
localization_priority: Normal
ms.assetid: 142bc0ce-7d16-4b69-9799-ce6558da2def
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 459e57d41ef7497c535e51944bbaf24daee84167
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782185"
---
# <a name="programming-with-the-c-api-in-excel"></a>Programmation avec l’API C dans Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Vous pouvez utiliser le Kit de d�veloppement logiciel (SDK) XLL Microsoft Excel 2013 et l�API C pour cr�er des fonctions de feuille de calcul hautes performances pour Excel 2013. Les mises � niveau vers l�API C Excel 2013 illustrent le support permanent aux utilisateurs pour lesquels les performances des fonctionnalit�s tierces ou internes sont critiques.
  
## <a name="excel-programming-interfaces"></a>Interfaces de programmation Excel

Excel offre plusieurs options pour le développement d’applications qui interagissent avec lui. Les interfaces de programmation Excel ont été ajoutées aux versions antérieures dans l’ordre suivant :
  
- **Langage de macro XLM :** premier langage accessible par l�utilisateur pour l�extension d�Excel et la base de l�API C. Bien que toujours pris en charge dans Excel 2010, XLM a longtemps �t� remplac� par Visual Basic pour Applications (VBA). 
    
- **API C et XLL :** DLL int�gr�es � Excel. Ces DLL offrent l�interface la plus directe et la plus rapide pour l�ajout de fonctions de feuille de calcul hautes performances mais au prix d�une complexit� sup�rieure par rapport aux technologies plus r�centes. 
    
- **VBA :** objets de code Visual Basic associ�s � des objets de classeur Excel. VBA permet la capture d��v�nements, ainsi que la personnalisation et l�ajout de commandes et de fonctions d�finies par l�utilisateur. VBA est la plus fr�quemment utilis�e et la plus accessible des options d�extensibilit�. 
    
- **COM :** interop�rabilit� standard pour les applications Windows par lesquelles Excel expose ses �v�nements et objets. VBA utilise COM pour interagir avec Excel. Excel exporte les biblioth�ques de type COM qui peuvent vous aider � cr�er des ressources de code C++ COM et des applications qui peuvent contr�ler Excel de fa�on externe. 
    
- **Microsoft .NET Framework :** environnement de code g�r� multilingue con�u pour le d�veloppement rapide d�applications destin�es aux environnements distribu�s. C# est le langage de programmation principal pour le code bas� sur .NET Framework bien que plusieurs langages puissent �tre compil�s dans le langage interm�diaire Microsoft (MSIL). Excel 2013 peut acc�der aux ressources de code contenues dans des assemblys .NET Framework. 
    
## <a name="when-to-use-the-c-api"></a>Quand utiliser l’API C

La principale raison d��crire des XLL et d�utiliser l�API C est de cr�er des fonctions de feuille de calcul hautes performances. Bien que les fonctions XLL soient souvent appel�es des fonctions d�finies par l�utilisateur, la formation n�cessaire � la compr�hension et � la ma�trise de l�environnement de d�veloppement des XLL les rendent peu accessibles � la plupart des utilisateurs. Toutefois, les applications des fonctions hautes performances (et dans Excel 2013, la possibilit� d��crire des interfaces multithreads vers des ressources serveur puissantes) en font un axe essentiel de l�extensibilit� d�Excel. 
  
La révision de l’API C introduite dans Excel 2007 concernait les aspects liés à des calculs hautes performances plutôt que les fonctionnalités telles que l’interface utilisateur.
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a>Écriture de fonctions de feuilles de calcul hautes performances définies par l’utilisateur

L�API C d�Excel est le choix id�al lorsque vous souhaitez cr�er des fonctions de feuille de calcul hautes performances en cr�ant des compl�ments XLL. L�API C vous fournit l�acc�s le plus direct aux donn�es de feuille de calcul. Les XLL fournissent � Excel le moyen le plus direct d�acc�der aux ressources DLL. Les performances des XLL sont encore am�lior�es dans Excel 2013 gr�ce � l�ajout de nouveaux types de donn�es mais surtout gr�ce � la prise en charge de l�ex�cution des fonctions d�finies par l�utilisateur sur des serveurs group�s.
  
L’utilisation des XLL a un coût : L’API C ne possède aucune des fonctionnalités de développement rapide de niveau supérieur de VBA, COM ou .NET Framework. La gestion de la mémoire opère à faible niveau et, par conséquent, fait peser plus de responsabilité sur le développeur. La plupart des fonctionnalités d’Excel exposées par le biais de COM, ce qui les rend accessibles par le biais de .NET Framework et de VBA, ne sont pas exposées à l’API C.
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a>Accès aux serveurs multithreads à l’aide de fonctions de feuille de calcul XLL

La fonction de Recalcul multithread (MTR), qui a été introduite dans Excel 2007, vous permet de créer des fonctions de feuille de calcul XLL thread-safe. Vous pouvez utiliser ces fonctions pour accéder aux serveurs multithreads. Les sections suivantes décrivent plus en détail comment cela peut considérablement augmenter les performances observées par l’utilisateur. Pour les utilisateurs Excel qui ont parfois besoin d’une puissance de traitement considérable, la combinaison d’un XLL qui utilise MTR et d’un serveur de calcul puissant constitue une solution hautes performances.
  
### <a name="customizing-the-excel-user-interface"></a>Personnalisation de l’interface utilisateur Excel

Pour la plupart des versions d’Excel, l’API C n’a pas été le choix idéal pour la personnalisation de l’interface utilisateur. VBA a un meilleur accès aux objets et événements Excel. L’interface utilisateur apparue dans Excel 2007 est sensiblement différente des versions antérieures à la fois par son apparence et la technologie sous-jacente. Vous pouvez personnaliser cette interface en utilisant des ressources de code managé.
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a>Création d’applications accessibles sur Internet

Les services Excel, introduits dans Microsoft Office 2007, offrent aux utilisateurs la meilleure façon d’accéder aux classeurs et aux fonctionnalités d’Excel par les outils de navigation web standards. Avec les langages de développement et ressources .NET Framework, ces technologies représentent une partie importante du déploiement d’Excel pour les utilisateurs dans le futur.
  
### <a name="controlling-excel-from-external-applications"></a>Contrôle d’Excel à partir d’applications externes

Excel expose ses objets, méthodes et événements au moyen de l’interface COM. Vous pouvez, par conséquent, utiliser COM pour créer des applications autonomes qui peuvent démarrer et contrôler une session Excel ou contrôler une session Excel existante. Vous pouvez accéder à l’interface Excel exposée par COM dans plusieurs langages de développement, notamment C++ et VBA. De la même façon, C# et .NET Framework fournissent une interface Excel qui autorise l’accès à distance et le contrôle d’Excel.
  
## <a name="asynchronous-calling-of-excel"></a>Appel asynchrone d’Excel

Excel permet aux XLL d’appeler l’API C uniquement lorsque Excel a transmis le contrôle à la XLL. Une fonction de feuille de calcul qui est appelée par Excel peut effectuer un rappel vers Excel à l’aide de l’API C. Une commande XLL qui est appelée par Excel peut appeler l’API C. Les fonctions et commandes DLL et XLL appelées par VBA lorsque VBA a lui-même été appelé par Excel peuvent appeler l’API C. Par exemple, vous ne pouvez pas définir un rappel Windows chronométré dans votre XLL et appeler l’API C à partir de celle-ci, et vous ne pouvez pas appeler l’API C à partir d’un thread en arrière-plan créé par votre XLL. Il est déconseillé d’appeler Excel de façon asynchrone à l’aide de COM à partir d’une DLL ou d’une XLL.
  
Cela se révèle très restrictif, car il peut y avoir des applications dans lesquelles vous souhaitez qu’Excel réagisse à un événement asynchrone. Par exemple, vous pouvez souhaiter qu’Excel récupère un élément de données sur Internet et effectue un nouveau calcul à chaque modification de ces données. Vous pouvez également souhaiter qu’un thread en arrière-plan effectue un calcul et qu’Excel effectue un nouveau calcul à la fin.
  
Pour y parvenir, vous pouvez faire en sorte qu’Excel recherche fréquemment les modifications, mais cette approche est inefficace et contre-productive car Excel devra fréquemment interrompre son activité normale. Vous pouvez configurer l’exécution répétée de la commande à l’aide de l’API C ou de VBA bien que cette solution ne soit pas idéale.
  
Dans l’idéal, vous souhaiterez peut-être un processus externe plus efficace qui contrôle la modification des données et qui, pour cela, déclenche Excel afin de récupérer la mise à jour et effectuer un nouveau calcul. Vous pouvez effectuer cette action à l’aide d’une application qui sert d’interface vers Excel à l’aide de COM. COM n’est pas limité comme l’API C à passer des appels uniquement lorsqu’Excel lui a passé le contrôle. Les applications COM peuvent appeler des méthodes Excel chaque fois qu’Excel est prêt bien que ces appels de méthode puissent être ignorés si les boîtes de dialogue sont affichées, si les menus sont déroulés ou si une macro est exécutée.
  
## <a name="c-api-and-its-relation-to-xlm"></a>API C et sa relation avec XML

Le langage de macro Excel (XLM) a �t� le premier environnement de programmation accessible par l�utilisateur dans Excel. Il permettait aux utilisateurs de cr�er des commandes et fonctions personnalis�es dans des feuilles de macro sp�ciales ressemblant � des feuilles de calcul ordinaires. Les feuilles de macro XML sont toujours prises en charge dans Excel 2013. Vous pouvez utiliser toutes les fonctions de feuille de calcul habituelles telles que **SUM** et **LOG** dans une feuille de macro, en plus des �l�ments suivants qui ne peuvent pas �tre entr�s dans une feuille de calcul : 
  
- Fonctions d�informations de l�espace de travail comme **GET.CELL** et **GET.WORKBOOK**.
    
- Fonctions �quivalentes de commande qui permettent l�automatisation des op�rations utilisateur ordinaires comme **DEFINE.NAME** et **PASTE**.
    
- Fonctions relatives aux modules compl�mentaires comme **REGISTER**.
    
- Captures d��v�nement de commande comme **ON.ENRTY** et **ON.TIME**.
    
- Op�rations propres aux fonctions de macro comme **ARGUMENT** et **VOLATILE**.
    
- Op�rations de contr�le de flux comme **GOTO** et **RETURN**.
    
Une version limit�e de l�API C existait dans Excel�3. Toutefois, dans Excel�4, le langage XML a �t� associ� � l�API C. Depuis lors, les DLL ont pu appeler toutes les fonctions de feuille de calcul, les fonctions d�informations de feuille de macro et les commandes et elles ont pu d�finir des captures d��v�nement. Les DLL ne peuvent pas appeler des fonctions de contr�le de flux XLM � partir de l�API C. Ces fonctions et fonctions de feuille de macro sont pr�sent�es dans le fichier d�aide XLMacr8.hlp (anciennement nomm� Macrofun.hlp). Pour obtenir ce fichier d�aide, acc�dez au [Centre de t�l�chargement Microsoft](http://download.microsoft.com) et recherchez « XLMacr8.hlp ». 
  
> [!NOTE]
> Windows Vista et Windows 7 ne prennent pas en charge directement les fichiers .hlp, mais vous pouvez y rem�dier en t�l�chargeant le [programme d�aide Windows (WinHlp32.exe) pour Windows Vista](http://go.microsoft.com/fwlink/?LinkID=82148) ou le [programme d�aide Windows (WinHlp32.exe) pour Windows�7](http://www.microsoft.com/download/en/details.aspx?id=91) � partir de Microsoft. 
  
Les DLL appellent les �quivalents API C de ces fonctions et commandes � l�aide des fonctions de rappel **Excel4**, **Excel4v**, **Excel12** et **Excel12v** (les deux derni�res ont �t� introduites dans Excel 2007). Les constantes �num�r�es qui correspondent � chaque fonction et commande sont d�finies dans un fichier d�en-t�te et transmises en tant qu�arguments � ces rappels. Par exemple, **GET.CELL** est repr�sent� par **xlfGetCell**, **REGISTER** par **xlfRegister** et **DEFINE.NAME** par **xlcDefineName**.
  
Outre les fonctions de feuille de calcul et les fonctions et commandes de feuille de macro, l�API C fournit des �num�rations de fonction et de commande qui peuvent �tre appel�es uniquement en utilisant les rappels suivants dans une DLL. Par exemple, **xlGetName** permet � la DLL de d�terminer le nom et le chemin du fichier, ce qui n�cessaire lorsque vous enregistrez des commandes et fonctions dans Excel. 
  
Depuis l’introduction de Visual Basic pour Applications (VBA) dans Excel 5 et de l’éditeur Visual Basic (VBE) dans la version 8 (Excel 97), le moyen le plus simple pour les utilisateurs de personnaliser Excel consiste à utiliser VBA au lieu de XML. Par conséquent, la majeure partie de la nouvelle fonctionnalité introduite dans les versions ultérieures d’Excel est disponible par le biais de VBA, mais pas au moyen de XML ou de l’API C. Par exemple, plusieurs commandes, captures d’événements et fonctionnalités de boîte de dialogue améliorées sont disponibles en VBA, mais pas au moyen de XML ou de l’API C.
  
Pour plus d�informations, voir [Quelles sont les nouveaut�s de l'API C pour Excel 2013](what-s-new-in-the-c-api-for-excel.md).
  
## <a name="see-also"></a>Voir aussi



[Nouveautés dans l’API C pour Excel](what-s-new-in-the-c-api-for-excel.md)
  
[Fonctions de rappel de l’API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)


[Prise en main du kit de développement logiciel XLL Excel](getting-started-with-the-excel-xll-sdk.md)

