Title: These Weeks in Rust 127
Number: 127
Date: 2016-04-25
Category: This Week in Rust

Hello and welcome to our first multi-week issue of *This Week in Rust*!
[Rust](http://rust-lang.org) is a systems language pursuing the trifecta:
safety, concurrency, and speed. This is a weekly summary of its progress and
community. Want something mentioned? Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) or [send us an
email](mailto:corey@octayn.net?subject=This%20Week%20in%20Rust%20Suggestion)!
Want to get involved? [We love
contributions](https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md).

*This Week in Rust* is openly developed [on GitHub](https://github.com/cmr/this-week-in-rust).
If you find any errors in this week's issue, [please submit a PR](https://github.com/cmr/this-week-in-rust/pulls).

This week's edition was edited by: [Vikrant](https://github.com/nasa42) and [llogiq](https://github.com/llogiq).

# Updates from Rust Community

## News & Blog Posts

* Reminder: [Rust Belt Rust Conference CFP](http://cfp.rust-belt-rust.com/) is open until April 30!

## Notable New Crates & Project Updates

* [specs](https://github.com/slide-rs/specs) - a rusty parallel ECS with breaking performance ([ecs_bench](https://github.com/lschmierer/ecs_bench))
* [Epaste](https://github.com/zetok/epaste). Tool to encrypt data and encode it as base64, so that it could be pasted on pastebin.

# Crate of the Week

This week's Crate of the Week is [owning_ref](https://crates.io/crates/owning_ref), which contains a reference type that can carry its owner with it. Thanks to [Diwic](https://users.rust-lang.org/users/diwic) for the suggestion!

[Submit your suggestions for next week][submit_crate]!

[submit_crate]: https://users.rust-lang.org/t/crate-of-the-week/2704

# Call for Participation

Always wanted to contribute to open-source projects but didn't know where to start?
Every week we highlight some tasks from the Rust community for you to pick and get started!

Some of these tasks may also have mentors available, visit the task page for more information.

* [easy] [rust: Add error explanations for all error codes](https://github.com/rust-lang/rust/issues/32777).
* [easy] [rust: rustbuild seems to deal badly with poor internet connections](https://github.com/rust-lang/rust/issues/32834).
* [medium] [regex: Decrease memory usage of DFA with variable width delta encoding of instruction pointers](https://github.com/rust-lang-nursery/regex/issues/199).
* [less easy] [servo: Store a `Box<Iterator>` instead of `Box<CollectionFilter>` in `HTMLCollection`](https://github.com/servo/servo/issues/10477).
* [easy] [токамак: Test cases for CI](https://github.com/vertexclique/tokamak/issues/16).
* [easy] [rexiv2: Results should likely use our own aliased Error (and Result?) type](https://github.com/felixc/rexiv2/issues/16).
* [easy] [rexiv2: Provide access to full XML XMP packet](https://github.com/felixc/rexiv2/issues/14).

If you are a Rust project owner and are looking for contributors, please submit tasks [here][guidelines].

[guidelines]: https://users.rust-lang.org/t/twir-call-for-participation/4821

# Updates from Rust Core

186 pull requests were [merged in the last two weeks][merged].

[merged]: https://github.com/issues?q=is%3Apr+org%3Arust-lang+is%3Amerged+merged%3A2016-04-11..2016-04-25

## Notable changes

* [`pub(restricted)` (RFC 1422) implemented](https://github.com/rust-lang/rust/pull/32875)
* [Warn on type parameter defaults](https://github.com/rust-lang/rust/pull/32817), this will become an error in the future
* [RFC #1494 amendment implemented](https://github.com/rust-lang/rust/pull/32945), allows type ascription in macros (IIRC)
* [`de-`/`encode()` methods no longer break Serialization deriving](https://github.com/rust-lang/rust/pull/32908)
* [Macro hygiene bugs fixed](https://github.com/rust-lang/rust/pull/32923)
* [Avoid crashing due to duplicate external items](https://github.com/rust-lang/rust/pull/32970)
* [Fix multiple glob import](https://github.com/rust-lang/rust/pull/32814)
* [MIR debuginfo mostly works](https://github.com/rust-lang/rust/pull/32952) ([etc.](https://github.com/rust-lang/rust/pull/32803))
* [MIR Blocks no longer require END_BLOCK](https://github.com/rust-lang/rust/pull/33030)
* [MIR now has LLVM-agnostic type layout](https://github.com/rust-lang/rust/pull/32939)
* [Register duplicate item symbols anyway](https://github.com/rust-lang/rust/pull/32946)
* [Resolve compiler performance regression fixed](https://github.com/rust-lang/rust/pull/33064)
* [Syntax: Import prefixes are now paths](https://github.com/rust-lang/rust/pull/33044)
* [Don't report errors in constants at every use site](https://github.com/rust-lang/rust/pull/32877)
* [Handle over-aligned realloc failures on UNIX](https://github.com/rust-lang/rust/pull/32997)
* [String::truncate goes to greater lengths to not panic](https://github.com/rust-lang/rust/pull/32977)
* [`BinaryHeap::append(..)`](https://github.com/rust-lang/rust/pull/32987)
* [Faster `is_char_boundary()` with bit twiddling](https://github.com/rust-lang/rust/pull/32862)
* [Fixed `BufRead` overrun on `Take`](https://github.com/rust-lang/rust/pull/32855)
* [`Default` for `RwLock`, `Mutex`, `CondVar`, `CStr`, `Path`](https://github.com/rust-lang/rust/pull/32785)
* [Cargo can now use multiple git user names](https://github.com/rust-lang/cargo/pull/2584)
* [Removed the (apparently broken) `std::net::IPV6_V6ONLY` feature](https://github.com/rust-lang/rust/pull/33124)
* [Handle `DefId`s and extern crates before lowering the AST to HIR](https://github.com/rust-lang/rust/pull/33089)
* [Compiletest now uses JSON output](https://github.com/rust-lang/rust/pull/33020)
* [`VecDeque::contains(_)` and `LinkedList::contains(_)` implemented](https://github.com/rust-lang/rust/pull/32951)
* [Rust now bootstraps from previous stable instead of snapshots](https://github.com/rust-lang/rust/pull/32942)
* [`impl From<Vec<T>>` and `Into<Vec<T>>` for `VecDeque<T>`](https://github.com/rust-lang/rust/pull/32866)
* [`BTree::append(_)` implemented](https://github.com/rust-lang/rust/pull/32466)

## New Contributors

* Timon Van Overveldt
* Tom Tromey
* Varun Vats
* vlastachu

## Approved RFCs

Changes to Rust follow the Rust [RFC (request for comments)
process](https://github.com/rust-lang/rfcs#rust-rfcs). These
are the RFCs that were approved for implementation this week:

* [RFC 1513: Stabilize implementing panics as aborts](https://github.com/rust-lang/rfcs/pull/1513).
* [RFC 1444: Provide native support for C-compatible unions, defined via a new keyword `untagged_union`](https://github.com/rust-lang/rfcs/pull/1444).
* [RFC 1398: Add a standard allocator interface and support for user-defined allocators](https://github.com/rust-lang/rfcs/pull/1398).
* [Amend RFC 550 with misc. follow set corrections](https://github.com/rust-lang/rfcs/pull/1494).

## Final Comment Period

Every week [the team](https://rust-lang.org/team.html) announces the
'final comment period' for RFCs and key PRs which are reaching a
decision. Express your opinions now. [This week's FCPs][fcp] are:

[fcp]: https://github.com/rust-lang/rfcs/labels/final-comment-period

* [Add `#[repr(pack = "N")]`](https://github.com/rust-lang/rfcs/pull/1399).
* [Feature gate extern fn methods](https://github.com/rust-lang/rfcs/pull/1429).
* [Allow Drop types in statics/const functions](https://github.com/rust-lang/rfcs/pull/1440).
* [Add a new crate-type, rdylib](https://github.com/rust-lang/rfcs/pull/1510).
* [Add workspaces to Cargo](https://github.com/rust-lang/rfcs/pull/1525).
* [Stabilize the `-C overflow-checks` command line argument](https://github.com/rust-lang/rfcs/pull/1535).
* [Add more integer atomic types](https://github.com/rust-lang/rfcs/pull/1543).
* [Add a generic `Atomic<T>` type](https://github.com/rust-lang/rfcs/pull/1505).
* [Remove some kinds of doc comments](https://github.com/rust-lang/rfcs/pull/1373).
* [Amend RFC 1228 with operator fixity and precedence](https://github.com/rust-lang/rfcs/pull/1319).

## New RFCs

* [Support code generators with source maps and multiple source directories](https://github.com/rust-lang/rfcs/pull/1573).
* [Introduce more conventions around documenting Rust projects](https://github.com/rust-lang/rfcs/pull/1574).
* [Add a `vis` matcher to `macro_rules!` that matches valid visibility annotations](https://github.com/rust-lang/rfcs/pull/1575).
* [Add a `literal` fragment specifier for `macro_rules!` patterns that matches literal constants](https://github.com/rust-lang/rfcs/pull/1576).
* [Rust memory model](https://github.com/rust-lang/rfcs/pull/1578).

# Upcoming Events

* [4/12. (San Diego) Eat– Drink– Rust! Downtown Rust Meetup](http://www.meetup.com/San-Diego-Rust/events/229907308/).
* 4/13. Introduction to Rust, The Arts and Science University of Chiapas.
* 4/13. Rust Community Team Meeting at #rust-community on irc.mozilla.org.
* [4/13. Rust Boulder/Denver Monthly Meeting](http://www.meetup.com/Rust-Boulder-Denver/).
* [4/14. Columbus Rust Society](http://www.meetup.com/columbus-rs/).
* [4/15. Frankfurt/Main Rust Lint Workshop](http://www.meetup.com/de-DE/Rust-Rhein-Main/events/229564640/?eventId=229564640)
* [4/18. Rust Paris](http://www.meetup.com/Rust-Paris).
* [4/20. OpenTechSchool Berlin: Rust Hack and Learn](http://www.meetup.com/opentechschool-berlin/).

If you are running a Rust event please add it to the [calendar] to get
it mentioned here. Email [Erick Tryzelaar][erickt] or [Brian
Anderson][brson] for access.

[calendar]: https://www.google.com/calendar/embed?src=apd9vmbc22egenmtu5l6c5jbfc%40group.calendar.google.com
[erickt]: mailto:erick.tryzelaar@gmail.com
[brson]: mailto:banderson@mozilla.com

# fn work(on: RustProject) -> Money

* [Software Engineer](http://www.coturnix.fr/en/#join) at Coturnix.
* [Senior full stack developer](http://onesignal.applytojob.com/apply/gpSzt4/Senior-Full-Stack-Developer) at OneSignal.
* [PhD and postdoc positions](http://plv.mpi-sws.org/rustbelt/) at MPI-SWS.

*Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) to get your job offers listed here!*

# Quote of the Week

*No quote was selected for QotW.*

[Submit your quotes for next week][submit]!

[submit]: http://users.rust-lang.org/t/twir-quote-of-the-week/328